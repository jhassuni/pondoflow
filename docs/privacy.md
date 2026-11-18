---
title: Privacy policy — Pondo Flow
permalink: /privacy
---

# Privacy Policy — Pondo Flow

**Last updated:** 18 November 2026
**Applies to:** Pondo Flow for Android (`com.fundledger.app`), version 1.0.0 and later.

This policy describes what Pondo Flow does with your data. It is written in plain
language, and every sentence in it was checked against the code that ships in the
app (see [Appendix A](#appendix-a--where-each-statement-comes-from)).

---

## 1. In short

- Your books stay **on your device**. Pondo Flow has no account, no server and
  no network access.
- The app **does not collect** your data, does not send it anywhere, does not
  show ads and contains no analytics or tracking.
- Your ledger is stored in an **encrypted database**.
- The only way data leaves the app is **something you ask for**: a backup, an
  export, or a report you save. You choose where it goes — or, for the reports
  CSV, which app you share it with.
- You can **delete everything** the app holds on your device, at any time, from
  Settings › *Delete Account & Data*.

## 2. The data the app holds on your device

Pondo Flow keeps the following on your device, so it can show your books:

| What | Examples |
| --- | --- |
| Ledger | Funds, projects, cash ledgers (cash on hand, bank accounts), the chart of accounts |
| Entries | Money in, money out, transfers between funds, starting balances, the memo, the category, the date |
| Receipt photos | A picture of a receipt you took or picked, attached to an entry — at most five per entry; a backup you export can carry the picture with it |
| Obligations | Bills to pay and amounts to collect, with the payee, the amount and the due date |
| Budgets | Budget amount, fund, project, expense category and period |
| Contacts | Name, phone number, email address, notes, type, and a photo you may add |
| Audit log | What changed, when it changed, and who changed it (always "This device") |
| Settings | Your currency, your language, your app-lock choice, the backup folder you picked |

Nothing else is collected: the app asks for no name, no email address, no
account, no advertising ID and no device ID of its own.

## 3. What the app never does

- **No account.** There is no sign-up and no login. Nothing is created on a
  server, because there is no server.
- **No network.** The app does not hold the `INTERNET` permission, so it
  *cannot* send anything over the network. The system permissions the app
  asks for are `USE_BIOMETRIC`, `USE_FINGERPRINT`, `WAKE_LOCK`,
  `ACCESS_NETWORK_STATE`, `RECEIVE_BOOT_COMPLETED` and `FOREGROUND_SERVICE`
  — all of them normal permissions, which grant nothing by themselves and are
  never shown to you as a prompt. The first two are the app lock; the last
  four are declared by WorkManager, the scheduler that runs the app's own
  automatic backups, so it can hold a wake lock, read whether the device is
  connected (`ACCESS_NETWORK_STATE` only reads the connection state — it
  cannot open a connection) and finish a job after a reboot. The app also
  declares one signature permission of its own, which only the app itself can
  hold.
- **No camera and no photo-library permission.** A receipt photo is taken with
  the camera app of your phone and picked with the photo picker of your phone.
  The app declares no `CAMERA` permission and no permission to read the media
  of your phone, so Android never asks you to grant one for a receipt — and the
  picker hands over only the single picture you chose.
- **No analytics, no ads, no crash reporting.** There is no tracking library in
  the app, and nothing about your use of it is measured.
- **No third-party SDK that phones home.** The only third-party native library
  the app ships is SQLCipher, the encryption library itself; every other
  dependency (AndroidX, Hilt/Dagger, Compose, Room, WorkManager, Coil) runs on
  the device. Coil only draws the contact photo you added — it cannot fetch
  anything from the internet, because the app has no internet access.
- **No cloud backup and no sync in this release.** The code for them exists but
  is switched off in the build that ships.

## 4. How your books are protected

- **The ledger is encrypted.** Your books live in a SQLCipher-encrypted
  SQLite database (`fundledger_secure.db`). The key is 32 random bytes that
  are wrapped by an AES-256 key held in the **Android Keystore**, which cannot
  be exported from the device. Only the wrapped key is stored on disk.
- **If the key is lost, the app refuses to open the ledger** — it never falls
  back to opening it unencrypted.
- **App lock (optional).** Turn it on in Settings › *Biometric App Lock* and the
  app asks for your fingerprint, your face or the device PIN before it opens
  your books, whenever the app comes back to the foreground. While the lock is
  closed, the app closes the database and keeps no key in memory.
- **Privacy mode (on by default).** Screenshots and the preview of the app in
  the recent-apps list are blocked, so your books cannot leave the screen by
  accident. You can turn it off in Settings › *Device & Privacy* — but not
  while the app lock is on.
- **Protected contacts.** A contact can be marked *Protected*; its record and
  the entries that point at it then need a biometric or device-PIN confirmation
  before they are shown again.
- **Receipt photos are encrypted too.** A receipt picture is kept in the app's
  own private storage as an **encrypted file** — AES-256-GCM, under a key that
  lives in the Android Keystore and cannot be exported from the device. Before
  it is encrypted the picture is shrunk to at most 1600 pixels on its long side
  and re-encoded as a JPEG, which drops the metadata of the photo — the place
  it was taken, the device and the time. It is decrypted in the memory of the
  app only while you are looking at it, and no unencrypted copy is written
  anywhere. A backup copy is encrypted again, with the backup's own key (§5).
- **The temporary copy of a photo is deleted at once.** The camera app writes
  the picture into a temporary file in the app's own cache; the app reads it,
  encrypts it and deletes that temporary file immediately — and also when you
  close the camera without taking a picture. If the app is killed while the
  camera is open, the leftovers are swept the next time you open the app.

**One honest exception:** a contact photo you add is copied into the app's own
private storage **unencrypted** (it is a plain image file, not part of the
encrypted database). Everything else above is inside the encrypted database or
in an encrypted file. If you add a photo of a sensitive document, remove it
again with Settings › *Delete Account & Data*.

## 5. Backups and exports — only when you ask

Every file the app writes outside its own storage is a file you asked for.

- **You choose the backup folder.** Pondo Flow uses Android's own folder
  picker; the app never picks a folder on its own and never scans shared
  storage.
- **Automatic snapshots are off until you turn them on.** With the setting on,
  the app writes a plain-text JSON snapshot into the folder you picked — once
  when you open the app and once a day — and keeps the newest five. It skips
  the snapshot while the app lock keeps your books closed; no photo is in it.
- **Manual exports** mostly go through Android's own file picker, so you
  choose the file name and the place every time. Settings › *Export & Import*
  writes a **backup** (your books and your receipt photos in one ZIP), a JSON
  file, or a ZIP of CSV tables; the Entries, Cash & Bank and Contacts screens
  also write a PDF, a CSV or an Excel workbook.
- **The reports CSV takes a second route.** The *Export CSV* action of the
  Reports screen writes the reports it is showing as plain-text CSV files into
  the app's own cache and hands them to Android's share sheet
  (`Intent.ACTION_SEND_MULTIPLE`), so **you pick the app that receives them**
  — a mail app, a messenger, a drive. The app grants that one app read access
  to those files for the time of the share, and the files are removed from the
  cache when the share is over. Nothing is shared on its own: the share sheet
  only opens after you tap the export.
- **A restore** (Settings › *Import backup*) reads a file you picked — a
  backup ZIP or a plain JSON backup — and replaces your current books with it,
  after you confirm. Keep a backup of the current state first if you are
  unsure. A restore takes everything or nothing: a backup that does not match
  its own list of photos, or a photo that was changed, is refused, and your
  books stay as they are.
- **These files are plain text** — with one exception. A JSON backup and a CSV
  export are readable by any text editor: they carry your entries, amounts and
  memos, and a JSON backup also carries your contacts and the newest rows of
  the audit log. The photo files inside a backup ZIP are the exception: they
  are encrypted with a key of the backup's own — and that key sits in the same
  ZIP, beside them. Anyone who has the backup file can open the photos in it,
  exactly as they can read the JSON next to them. Treat every backup like a
  paper statement: store it somewhere only you can reach.
- **A receipt picture travels in the backup ZIP.** Settings › *Export backup*
  writes a ZIP: `backup.json` — the snapshot, in plain text — plus one
  `attachments/<id>.enc` file per receipt photo. The dialog before the export
  tells you how many photos are on the device and how much space they take, and
  a restore re-encrypts every photo with the key of the phone that reads it.
  Nothing is uploaded: the ZIP is only a file you asked for, in the place you
  picked. The plain *Export JSON* file and the automatic snapshots carry only
  the **record** of a photo, so a restored ledger lists the receipt and the app
  says *Photo not on this device*.

## 6. Deleting your data

Settings › *Delete Account & Data* erases **everything** Pondo Flow holds on
your device: the encrypted ledger and its sidecar files, the cached exports,
your preferences, the contact photos, the receipt photos, the key material of
the ledger, and the permission the app holds on your backup folder. It asks you
to type `DELETE` first, and it cannot be undone.

Because there is no account on a server, there is nothing to erase there: all
of your data is on your device, and all of it is deleted here.

Removing the app also removes its private storage. Files you exported or
backed up yourself stay where you put them — they are yours to delete.

## 7. Children's privacy

Pondo Flow is a bookkeeping tool for adults who manage real money: it is not
directed at children, and it is not intended for users under 13 (or the
minimum age of your country). We do not knowingly collect data from children,
because we do not collect data from anyone.

## 8. Changes to this policy

If a future version of the app changes what it does with your data, this
document and the store listing will be updated before that version is
published, and the "Last updated" date above will change.

## 9. Contact

Questions about this policy, or about the data Pondo Flow holds, can be sent to:

**support@sigbin.net**

sigbin.net
Mandaue City, Cebu, Philippines

---

## Appendix A — where each statement comes from

Every claim above was checked in the code of `main` at commit `6bb1b07c` (the
backups with the receipt photos merged as `0745bf1e`). Paths are relative to the repository
root.

| # | Statement | Where it lives in the code |
| --- | --- | --- |
| 1 | The app's own manifest declares `USE_BIOMETRIC` and `USE_FINGERPRINT`; the merged manifest of the shipped APK asks for those two plus `WAKE_LOCK`, `ACCESS_NETWORK_STATE`, `RECEIVE_BOOT_COMPLETED` and `FOREGROUND_SERVICE` — the last four are declared by WorkManager 2.10.0 — and **no `INTERNET`** | `app/src/main/AndroidManifest.xml:18-19`; `gradle/libs.versions.toml:24,75` (`androidx.work:work-runtime-ktx` 2.10.0), `app/build.gradle.kts:188`; the merged manifest of the built APK (`app/build/intermediates/merged_manifest/**/AndroidManifest.xml`) |
| 2 | `allowBackup=false`, backup rules exclude every domain, cleartext traffic is denied | `app/src/main/AndroidManifest.xml:39-47`, `app/src/main/res/xml/data_extraction_rules.xml`, `app/src/main/res/xml/backup_rules.xml`, `app/src/main/res/xml/network_security_config.xml` |
| 3 | No runtime permission is ever requested | no `requestPermissions` / `Manifest.permission` call in `app/`, `core/`, `feature/` |
| 4 | No analytics, ads, crash-reporting or HTTP client | no matching dependency in `gradle/libs.versions.toml`; no matching import in any `src/main` source |
| 5 | The `sync` module only reads and writes local database rows; the premium tier is a build switch that is off by default | `sync/src/main/kotlin/com/fundledger/sync/CloudSyncCoordinator.kt`, `sync/src/main/kotlin/com/fundledger/sync/PremiumTier.kt`, `sync/build.gradle.kts` (`PREMIUM_ENABLED`), `build.gradle.kts` (`premiumEnabledParsed`) |
| 6 | The premium/cloud card is not shown when the switch is off | `feature/settings/src/main/kotlin/com/fundledger/feature/settings/PremiumSettings.kt:114,193`, `feature/settings/src/main/kotlin/com/fundledger/feature/settings/SettingsScreen.kt:1338` |
| 7 | The ledger is encrypted with SQLCipher | `gradle/libs.versions.toml` (`net.zetetic:sqlcipher-android` 4.13.0), `core/data/src/main/kotlin/com/fundledger/core/data/security/SqlCipher.kt` |
| 8 | 32 random bytes, wrapped by an AES-256-GCM Keystore key; only the ciphertext is stored | `core/data/src/main/kotlin/com/fundledger/core/data/security/DbKeyManager.kt:141,311-326,369,379` |
| 9 | The database is opened through `SupportOpenHelperFactory(passphrase)` | `core/data/src/main/kotlin/com/fundledger/core/data/security/LedgerOpenHelperFactory.kt:110` |
| 10 | A lost Keystore key blocks the app; the ledger is never opened in the clear | `core/data/src/main/kotlin/com/fundledger/core/data/security/DbKeyManager.kt:114-176`, `core/data/src/main/kotlin/com/fundledger/core/data/security/LedgerState.kt` |
| 11 | The database file name | `core/data/src/main/kotlin/com/fundledger/core/data/local/AppDatabase.kt:109` |
| 12 | App lock: off on a fresh install, opt-in, closes the database while locked | `core/data/src/main/kotlin/com/fundledger/core/data/security/AppLockStore.kt:259-264`, `core/data/src/main/kotlin/com/fundledger/core/data/security/LedgerBootstrap.kt:119-126` |
| 13 | App lock uses `androidx.biometric` 1.1.0, `BIOMETRIC_STRONG` or `DEVICE_CREDENTIAL`, 60 s background timeout, 5 attempts | `gradle/libs.versions.toml:26,78`, `core/data/src/main/kotlin/com/fundledger/core/data/security/AppAuthenticator.kt:653-684`, `core/common/src/main/kotlin/com/fundledger/core/common/AppConstants.kt:15-16` |
| 14 | Privacy mode is on by default and applies `FLAG_SECURE` | `core/data/src/main/kotlin/com/fundledger/core/data/security/PrivacyModeStore.kt:127-129`, `core/common/src/main/kotlin/com/fundledger/core/common/security/PrivacyModePolicy.kt:30-47`, `app/src/main/kotlin/com/fundledger/app/PrivacyMode.kt:18-27` |
| 15 | A protected contact needs a biometric or device-PIN confirmation | `feature/contacts/src/main/kotlin/com/fundledger/feature/contacts/ContactUnlockGate.kt` |
| 16 | Contact photos are copied into `filesDir/contact_photos` **in the clear** | `feature/contacts/src/main/kotlin/com/fundledger/feature/contacts/ContactsScreen.kt:223,836`, `core/data/src/main/kotlin/com/fundledger/core/data/wipe/LocalDataWipe.kt:494-497` |
| 17 | The backup folder is chosen with the system folder picker; the snapshot is plain-text JSON | `feature/settings/src/main/kotlin/com/fundledger/feature/settings/SettingsScreen.kt:906` (`OpenDocumentTree`), `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:164-192` |
| 18 | Automatic snapshots are opt-in; once a day and on app open; the newest five are kept; a locked ledger defers the snapshot | `app/src/main/kotlin/com/fundledger/app/BackupScheduler.kt:65-116`, `app/src/main/kotlin/com/fundledger/app/BackupWorker.kt:42-67`, `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:1717` (`pruneAutoBackups(keep = 5)`), `:1071` |
| 19 | The backup, the entries, the cash & bank and the contact exports go through the system file picker; the user picks the destination every time | `feature/settings/src/main/kotlin/com/fundledger/feature/settings/SettingsScreen.kt:854,876,898`, `feature/transactions/.../TransactionsScreen.kt:925-933`, `feature/dashboard/.../TreasuryScreen.kt:462-468`, `feature/contacts/.../ContactsScreen.kt:404-412` |
| 20 | What a JSON backup contains (funds, projects, accounts, transactions, entries, payables, receivables, budgets, contacts, contact types, audit log, closed periods) and that the audit log is capped at the newest 10,000 rows in an export | `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:164-192`, `:1120-1160`, `:1761` |
| 21 | What the CSV ZIP contains (funds, projects, accounts, transactions, entries, payables, receivables, budgets) | `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:920-950` |
| 22 | A restore replaces the current data, after a confirmation | `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:387,499-596`, `feature/settings/src/main/kotlin/com/fundledger/feature/settings/SettingsScreen.kt:996-998` |
| 23 | The audit log is append-only at the storage layer, with unbounded retention | `core/data/src/main/kotlin/com/fundledger/core/data/local/entity/Entities.kt:430-460`, `core/data/src/main/kotlin/com/fundledger/core/data/AuditLogWriter.kt:26-47` |
| 24 | An audit row of a transaction carries the amount, and its detail carries the description or memo | `core/accounting/src/main/kotlin/com/fundledger/core/accounting/TransactionService.kt:2027-2028,2214-2215,2441-2442` |
| 25 | The wipe deletes the ledger, the caches, the preferences, the private storage (with the contact photos), the key material and the backup-folder grants; it is local only | `core/data/src/main/kotlin/com/fundledger/core/data/wipe/LocalDataWipe.kt:31-95,310-361,386-406,453-506` |
| 26 | The app asks the user to type `DELETE` before the wipe | `feature/settings/src/main/res/values/strings.xml` (`settings_delete_data_confirm_label`) |
| 27 | A release build writes nothing to the platform log; no amount, memo, name, phone number or email is logged | `core/data/src/main/kotlin/com/fundledger/core/data/log/SecureLog.kt:1-98`, `app/src/test/kotlin/com/fundledger/app/SecureLoggingGuardTest.kt` |
| 28 | The 10 shipped languages | `app/src/main/res/values*/strings.xml`, `feature/settings/src/main/kotlin/com/fundledger/feature/settings/LanguageSettings.kt:53` |
| 29 | The **Restore** action of the audit log restores an **entry** or a **contact**; any other kind is refused | `feature/settings/src/main/kotlin/com/fundledger/feature/settings/AuditLogScreen.kt:86-94` |
| 30 | A fund can be archived and brought back (un-archived); no money moves | `feature/funds/src/main/kotlin/com/fundledger/feature/funds/FundsScreen.kt`, `feature/settings/src/main/res/values/strings.xml` (`settings_unarchive_body`) |
| 31 | The *Export CSV* action of the Reports screen stages the reports it is showing as plain-text CSV files in the app's own cache and hands them to another app through the system share sheet (`Intent.ACTION_SEND_MULTIPLE` / `createChooser`, `FLAG_GRANT_READ_URI_PERMISSION`); the receiving app is the one the user picks, and the files are served through the `FileProvider` of the app, which is not exported | `feature/reports/src/main/kotlin/com/fundledger/feature/reports/ReportsExportAction.kt:287-297`, `core/data/src/main/kotlin/com/fundledger/core/data/export/ReportCsvShareManager.kt:148,231`, `app/src/main/AndroidManifest.xml:68-76` |
| 32 | A receipt photo is **taken** with the camera app of the phone (`ActivityResultContracts.TakePicture`) and **picked** with the photo picker of the phone (`ActivityResultContracts.PickVisualMedia`, images only) | `feature/transactions/src/main/kotlin/com/fundledger/feature/transactions/ReceiptPhotos.kt:938,986-987,1054-1056` |
| 33 | The picker grants only the one picture the user picked and asks for no permission to read the storage of the phone | `feature/transactions/src/main/kotlin/com/fundledger/feature/transactions/ReceiptPhotos.kt:894-896,213-219` |
| 34 | The app's own manifest declares **no camera permission and no media permission** — only `USE_BIOMETRIC` and `USE_FINGERPRINT` — and the merged manifest of the shipped APK asks for those two plus the four WorkManager permissions, with no `CAMERA` and no `READ_MEDIA_*` | `app/src/main/AndroidManifest.xml:18-19`; the merged manifest of the built APK (`app/build/intermediates/merged_manifests/**/AndroidManifest.xml`) |
| 35 | The camera writes the picture into a temporary file in the app's own cache, through the `FileProvider`; the copy is read once and deleted at once, and also when the reader cancels the camera; the leftovers of a killed session are swept when the photo section is opened and at the start of the app | `feature/transactions/src/main/kotlin/com/fundledger/feature/transactions/ReceiptPhotos.kt:1016-1024,1196-1202,952-959,1358-1370,1376-1378,390-399`; `app/src/main/kotlin/com/fundledger/app/FundLedgerApplication.kt:202-235` |
| 36 | The picture is shrunk to 1600 px, re-encoded as JPEG (which drops the EXIF — the place, the device and the time), encrypted with AES-256-GCM under a Keystore key that cannot leave the device, and written to the private storage as `filesDir/attachments/<id>.enc` | `core/data/src/main/kotlin/com/fundledger/core/data/attachments/ReceiptPhotoStore.kt:36-40,84-86,260-289,309-315,334-350,457-461` |
| 37 | The picture is read back decrypted **in memory only** and the viewer writes it nowhere; the user can open it full-screen and delete it, and the delete asks first, removes the encrypted file and soft-deletes the record; five photos per entry | `core/data/src/main/kotlin/com/fundledger/core/data/attachments/ReceiptPhotoStore.kt:129-159,161-182,459`; `feature/transactions/src/main/kotlin/com/fundledger/feature/transactions/ReceiptPhotos.kt:660-664,505-531,671-749,757-780` |
| 38 | The plain JSON backup and the automatic snapshot carry the attachment **rows** but no photo file, so a restored row reads as *Photo not on this device* | `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:182,1240-1241,1345`; `feature/transactions/src/main/kotlin/com/fundledger/feature/transactions/ReceiptPhotos.kt:634-639`, `feature/transactions/src/main/res/values/strings.xml:230` |
| 39 | The wipe deletes the whole private storage, so the receipt photos go with it; deleting an entry removes the photos of that entry | `core/data/src/main/kotlin/com/fundledger/core/data/wipe/LocalDataWipe.kt:506-507`; `core/accounting/src/main/kotlin/com/fundledger/core/accounting/TransactionService.kt:4344`, `core/data/src/main/kotlin/com/fundledger/core/data/attachments/ReceiptPhotoStore.kt:205-246` |
| 40 | A backup that carries the photos is a **ZIP**: `backup.json` — the snapshot, in plain text — plus one `attachments/<id>.enc` file per photo; the export dialog shows how many photos and how much space the file will take; a restore of it takes everything or nothing (the refusals of the archive, and the removal of what a refused restore had already written) | `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupPhotoArchive.kt:44-47,86,88-92,196-235`; `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupExportManager.kt:330-363,442-486`; `feature/settings/src/main/kotlin/com/fundledger/feature/settings/SettingsScreen.kt:1034-1056`; `feature/settings/src/main/res/values/strings.xml:93,96-99` |
| 41 | The photos in that ZIP are encrypted with the **backup's own key**, and that key travels inside the same ZIP; a restore re-encrypts every photo with the key of the phone that reads it | `core/data/src/main/kotlin/com/fundledger/core/data/export/BackupPhotoArchive.kt:98-101,134,205`; `core/data/src/main/kotlin/com/fundledger/core/data/attachments/ReceiptPhotoStore.kt:189-222` |
