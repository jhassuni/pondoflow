# Pondo Flow — Frequently Asked Questions

Plain answers to the questions people ask most. For the full walkthrough, see the
[User Guide](GUIDE.md).

## Your data

### Is my data online?

No. Pondo Flow keeps everything on your phone. There is no account to create and no server
that holds a copy of your books, so nobody else can read them — and the app works with the
internet turned off.

### What if I lose my phone, or it breaks?

Your books are gone with the device, unless you have a backup. Set up **Auto-Backup (Safety
Net)** in **⋮ → Settings → Backup**, or export a backup yourself with **Export backup** — one
ZIP with your books and your receipt photos. Then install Pondo Flow on the new phone and use
**Import backup** to bring your books and photos back.

Pondo Flow keeps the key of your ledger on the device as well, so a new install cannot open
the old ledger on its own — it needs the backup you saved.

### Can I use Pondo Flow on two phones at the same time?

No. Every install has its own books, and there is no server copy that keeps them in step. If
you want the same books on a second phone, export a backup on the first phone and import it on
the second. Keeping your books in step across your phones is planned for the next big update
(Premium).

### Can my partner and I share one ledger?

Not in the app today. The books live on one device. You can both look at them, or you can export
a copy of the entries, a report, or the contacts list to share. Sharing one set of books with your
household or organization is planned for the next big update (Premium).

### Does Pondo Flow work without internet?

Yes, all of it. There is nothing to download and nothing to sync.

### How do I keep a backup?

Open **⋮ → Settings → Backup**. **Back Up Now** writes a snapshot at once. Turn on
**Automatic snapshots** and choose a folder you control, and Pondo Flow writes a snapshot
when the app opens and once a day.

After you reinstall the app, pick the same folder again and use **Restore Latest**.

### Is my backup file safe to keep in Google Drive?

It is a plain copy of your books, so treat it the way you would treat a paper ledger: keep it
somewhere only you can reach. The database on your phone is encrypted; the backup file is the
one readable copy, by design. A backup made with **Export backup** also carries your receipt
photos, and anyone who has the file can open them too.

## Locking and privacy

### What if I forget my PIN?

Pondo Flow does not have a PIN of its own. The app lock uses your device's screen lock — your
fingerprint, your face, or the PIN you already set on the phone. If you cannot get into the
device, that is the device's own recovery to sort out; Pondo Flow cannot unlock it for you.

### What happens if I try to open the app too many times with the wrong fingerprint?

Pondo Flow asks you to use the PIN of the device instead. The app lock is there to keep your
books private, not to lock you out of your own data.

### Can I stop anyone from taking screenshots of my books?

Yes. Turn on **Privacy mode** in **⋮ → Settings → General → Device & Privacy**. Screenshots and
the preview in the recents are blocked while it is on.

### Can I unlock a period I closed by mistake?

Yes. Open **⋮ → Settings → Bookkeeping → Books**, find the period under **Closed periods**, and
tap **Unlock**. Pondo Flow asks you to confirm who you are, and writes the unlock to the
audit log.

## Money in, money out, and reports

### What is the difference between Money In and Income?

On **Home**, **Money In (Month)** is the cash that came in during the month — a receipt, a
collection, or a starting balance you entered. On the **Reports** tab, **Total Income** is
the stricter accounting figure: a starting balance is not income there, it is part of what you
started the period with.

### Why does a report show this total?

Every amount on a report is a tap target. Tap it and a popup opens showing the entries behind
that exact amount, with their **Total** at the bottom. From the popup you can **View in
Entries** or **View in Payables**. If the number looks wrong, the popup usually tells you
why.

### What is "Projected after obligations"?

It is the money you will have once the bills you still owe are paid and the amounts owed to
you are collected. It sits under **Available** on the fund and project cards. Only **Open**
bills count, and the figure can go negative — that is a real warning that your commitments
are bigger than your cash.

### Why did Pondo Flow warn me that I do not have enough money?

The amount is more than the fund holds. You can **Spend Anyway** if you know the money is
coming, or change the amount and the fund. The warning is there so an overspend is your
decision, not an accident.

### What is Cash Coverage?

It is how much of the bills coming due your **Total Balance** covers. When no bills are due,
Pondo Flow divides the balance by your average spending over the last three complete months
instead, and says so.

### Can I move money between funds?

Yes — **⇄ Move** in **Quick Entry**, or **Transfer** on a fund. Moving money between funds
does not change your total; it only changes which pot it is in. A transfer is not counted as
**Money In** or **Money Out**.

### Why is my Money In and Money Out total different from the report?

The two screens measure the same thing but show it in different places. If they ever disagree
for the same period, the **Cash in** and **Cash out** cards on **Reports** are the formal
figures, and tapping the amount there shows the entries behind it.

## Bills and amounts to collect

### What is the difference between a bill and something to collect?

A bill is money **you owe** — it is on **⋮ → Bills to Pay**. Something to collect is money
**owed to you** — it is on **⋮ → To Collect**. Both work the same way: a counterparty, an
amount, a due date, and a fund.

### I paid a bill. What now?

Open the bill and tap **Mark Paid**. Pondo Flow fills in the entry for you and asks you to
confirm where the money came from. An amount you collected is settled the same way with **Mark
Received**.

### I deleted a bill by mistake. Can I get it back?

Yes. Bills are never destroyed — they are deactivated. Open **⋮ → Audit Log**, find the
deactivated record and tap **Restore**.

### How do I set up a bill that repeats every month?

Open the bill, tap **Repeat**, and choose **Monthly**. Set **Ends** to **Never**, **On a
date** or **After a number of times**. Pondo Flow creates the next bill for you before it is
due, and it appears in your **Action Queue**.

### Can an entry repeat as well?

Yes. Set **Repeat** on the entry itself, with the same choices — **Weekly**, **Every 2
weeks**, **Monthly**, **Quarterly**, **Yearly**. The rules are listed under **⋮ → Repeating
entries** on the **Entries** tab, where you can **Pause** or **Resume** them. A rule set to
**Ask me first** waits for you on **Home**, where you **Post** or **Skip** it.

## Everyday use

### How do I attach a receipt to an entry?

Open the entry and tap **Add receipt photo**, then choose **Camera** or **Gallery**. An entry
can hold up to five photos, and you can remove one with **Delete photo**.

### How do I undo a mistake?

Every entry you save comes with an **Undo** in the message at the bottom of the screen. If you
missed it, open **⋮ → Audit Log** — the change is there, and a deactivated record can be
brought back with **Restore**.

### What is the audit log for?

It is the record of every change Pondo Flow made: what was **Created**, **Edited**,
**Deactivated** or **Restored**, and when. It is append-only and kept forever, so you can
always see what happened to a number and when.

### Why would I close a period?

Closing a period locks the entries and the audit rows inside it, so last month's numbers
cannot quietly change. Corrections to a closed period are posted as new entries in the current
period instead. You choose when to close — Pondo Flow never does it on its own.

### Can I give Pondo Flow a starting balance?

Yes, when you create a fund. A starting balance is money that was already in the pot, not
money that came in during the period, which is why it shows up differently on a report.

### How do I give my accountant the numbers?

On the **Reports** tab, use **Export CSV** or **Share reports** for a PDF. The **Entries** and
**Contacts** screens export the list you are looking at as a **PDF Document**, a **CSV File**
or an **Excel Workbook**. For the whole database, use **Export JSON** or **Export CSVs (.zip)**
in **⋮ → Settings → Backup**.

### Does Pondo Flow handle more than one currency?

Not at the same time — your books keep one currency (more than one currency is planned for the
next big update, Premium). Choose it in **⋮ → Settings → General →
Currency & Region**, either **Auto (Device Local)** or a currency you pick.

### Is Pondo Flow available in my language?

It ships in English, Español, Français, Português (Brasil) and العربية, and in five
community translations marked **Beta / Community Translated**: Kiswahili, हिन्दी, বাংলা,
Bahasa Indonesia and Русский. Change the language in **⋮ → Settings → General → Language**.

## Help

### How do I contact support or report a bug?

In the app, open **⋮ → Settings → About → About Pondo Flow → Contact support** — it opens your
email app with a message to **support@sigbin.net**. Or email us directly. Bugs and ideas can
also go to the public tracker: [open an issue](https://github.com/jhassuni/pondoflow/issues/new/choose).
