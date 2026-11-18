---
title: Terms of Use — Pondo Flow
permalink: /terms
---

# Terms of Use — Pondo Flow

**Last updated:** 18 November 2026
**Applies to:** Pondo Flow for Android (`com.fundledger.app`), version 1.0.0 and later.

These terms are the agreement between you and the publisher of Pondo Flow when you
download or use the app. They are written in plain language. The Privacy Policy
is separate: it covers what the app does with your data.

---

## 1. In short

- Pondo Flow is a **bookkeeping tool** for your own money, and **not** financial,
  tax, accounting or legal advice. It is free to use: there is no charge, no
  subscription and no in-app purchase.
- **You** are responsible for the entries you make and for keeping your own
  backups.
- Your books live **only on your device**. There is no server copy.
- The app is provided **"as is"**, without warranty, and it may be changed,
  updated or withdrawn.

## 2. What Pondo Flow is — and is not

Pondo Flow keeps the books of money you actually handle: what came in, what went
out, and what is left in each fund, project and cash ledger. It runs on your
device, offline. The free app has limits on how many funds, projects and cash
ledgers you can keep active at once; the app shows each limit next to the
count, and the limits may change between versions.

The reports it produces — **Income & Spending Summary**, **Statement of
Financial Position**, **Budget vs Actual** and the **Project statement** — are
**general bookkeeping statements**. They are not a tax return, a statement
prepared to a reporting standard, or an official filing for any country.
Turning them into one is a local, expert task that Pondo Flow does not do.

Pondo Flow does not give you financial, tax, accounting or legal advice, and it
does not make decisions for you. It records the numbers you enter and reports
on them. If you need an answer about what you owe, what you may claim, or how
your books must be presented, ask a qualified professional in your country.

## 3. Your responsibilities

- **Accuracy.** You are responsible for what you enter — the app cannot know
  whether a memo, a category or an amount is right, so check your entries.
- **Backups.** Your data lives on your device, and the key that opens it lives
  there too. If the phone is lost, broken, reset or uninstalled, your books go
  with it — there is no account and no server copy to restore them from —
  unless you kept a backup. Turn on automatic snapshots and choose a folder
  you control, or export a backup yourself, and keep it somewhere safe. A
  backup is a plain-text copy of your books: store it as carefully as paper.
- **Exported files.** Files you export or share — JSON, CSV, PDF, Excel — are
  yours and readable; they are outside the app's protection, and yours to
  delete.
- **Lawful use.** You must be entitled to keep the records you record and the
  photographs you attach.

## 4. Acceptable use

Use Pondo Flow for lawful bookkeeping of money you are responsible for. Do not
use it to store or distribute anything unlawful, or in a way that breaks the
law of your country. Every right and duty that comes with the records stays
with you.

## 5. No warranty, and the app may change

Pondo Flow is provided **"as is"**, without warranty of any kind, express or
implied, to the fullest extent the law allows. The app is a tool, not a
keeper of your records: we do not warrant that it will be uninterrupted or
error-free, or that it will preserve your data. Keeping copies is your job.

The app may also be updated, and its features may change or be withdrawn. The
terms in force are the ones published with the version you are using.

## 6. Limitation of liability

To the extent permitted by law, the publisher is not liable for loss of data,
lost profits, or any indirect or consequential loss arising from your use of
Pondo Flow or from decisions you make on the strength of its figures. Some
countries do not allow certain exclusions; where that is so, the exclusion does
not apply to you.

## 7. Google Play

Pondo Flow is downloaded from Google Play. Your download and your use of it are
also subject to **Google Play's Terms of Service** and to the Play policies,
which sit alongside these terms.

## 8. Changes to these terms

If these terms change, this document and the store listing are updated before
the change takes effect, and the "Last updated" date above changes with them.
Using the app after that means you accept the new terms.

## 9. Contact

Questions about these terms can be sent to:

**hello@joevin.me**

joevin.me
Mandaue City, Cebu, Philippines


---

## Appendix A — where each statement comes from

Every claim above was checked in the code of `main` at commit `703c443a`.

| # | Statement | Where it lives |
| --- | --- | --- |
| 1 | The app is free: no billing library, no `BILLING` permission, no in-app purchase, and the paid tier is switched off in the build that ships | `gradle/libs.versions.toml` (no billing dependency); `app/src/main/AndroidManifest.xml:18-19`; `build.gradle.kts:48` (`null -> false`), `sync/build.gradle.kts:33` (`PREMIUM_ENABLED`) |
| 2 | There is no account and no server copy: the app holds no `INTERNET` permission | `app/src/main/AndroidManifest.xml:18-19`; `feature/settings/src/main/res/values/strings.xml:187` ("There is no account on a server yet") |
| 3 | Your books go with the device unless you kept a backup, and the key stays on the device | `docs/user/FAQ.md:16-21`; `core/data/.../security/DbKeyManager.kt` |
| 4 | Automatic snapshots are opt-in, go to a folder you choose, and are plain text | `feature/settings/.../SettingsScreen.kt:906` (`OpenDocumentTree`); `app/.../BackupScheduler.kt:80,111`; `docs/store/PRIVACY_POLICY.md` §5 |
| 5 | The reports are general bookkeeping statements, not statutory or tax reporting | `docs/PRD.md:46-48` (non-goal: "Tax or statutory reporting for any jurisdiction") |
| 6 | The free app has limits on active funds, projects and cash ledgers | `core/common/.../AppConstants.kt:7-8,47`; `core/accounting/.../TransactionService.kt:760-766,1001-1007` |
