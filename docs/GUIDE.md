# Pondo Flow User Guide

Pondo Flow keeps your money records **on your own phone**. There is no account to create,
nothing is uploaded to a server, and the app works with the internet turned off. This guide
walks through the screens in the order you will meet them.

Every screen name and button in this guide is written exactly as the app shows it.

## Contents

- [Getting started](#getting-started)
- [Categories and the Chart of Accounts](#categories-and-the-chart-of-accounts)
- [Funds and projects](#funds-and-projects)
- [Entries](#entries)
- [Credit cards](#credit-cards)
- [Bills to pay and to collect](#bills-to-pay-and-to-collect)
- [Budgets](#budgets)
- [Reports](#reports)
- [Contacts](#contacts)
- [Backup and restore](#backup-and-restore)
- [Audit log and closing a period](#audit-log-and-closing-a-period)
- [Privacy mode](#privacy-mode)
- [About, privacy and support](#about-privacy-and-support)
- [Languages](#languages)

## Getting started

### Your first launch

Pondo Flow first asks **What are these books for?** and sets up your categories to match:

- **Personal / household** (chosen by default) — salary, food & groceries, rent, electricity,
  water, school…
- **Organization / group** — for a church, club, NGO or project: donations, grants, program,
  operations, travel, supplies…
- **Customize** — pick the categories yourself from both sets, with **All** / **None** for each
  group. Your own categories come later, from the entry form or from Settings.

**Skip** starts a personal book. You can add the other set later in Settings.

The **Home** screen then shows a three-card guide:

1. **1 of 3 · Purpose-Driven Funds** — give all your money a clear purpose.
2. **2 of 3 · Projects & Events** — tag spending by project.
3. **3 of 3 · Local-First & Private** — everything stays on your phone, export anytime.

Tap **Next →** to move on and **← Back** to go back. **Skip Guide** dismisses it at once. On
the last card, **Done** starts you off with the **General Fund**, and **+ New Fund** sets up
your own fund first.

### The Home screen

- **Total Balance** — the cash you hold, across money in hand and money in the bank.
- **Money In (Month)** and **Money Out (Month)** — what came in and what went out this month.
- **Credit cards** — next to your cash: the **Total owed** on your cards, and **Available**
  when a card has a limit. Tap a card to see its entries; with no card yet the tile offers
  **Add a credit card**.
- **Cash Coverage** — how much of the bills coming due your cash covers. What you owe on
  your credit cards counts here too, because it is money you will have to pay.
- **Action Queue** — what needs you: a bill to pay, an amount to collect, or a repeating entry
  to **Post** or **Skip**. A bill in the queue offers **Mark as Paid**, an amount to collect
  offers **Mark as Received**.
- **Recent Activity** — your latest entries. Tap **See All →** for the whole list.

Tapping a card opens the list of entries behind it.

### Currency

Open **⋮ → Settings → General → Currency & Region**. The card names the currency that is active
and shows a sample amount, so you can check the symbol and the formatting before you record
anything.

- Tap a quick choice: **Device** (the currency of your phone), **PHP**, **USD** or **EUR**.
- **More currencies…** opens a list you can search by country or currency.
- **+ Add custom currency** adds one of your own: a **code** of three letters, a **symbol** of
  up to four characters, and **0 to 3 decimals**.

The screen refreshes when you change the currency, so every amount shows the new symbol at
once. **Delete all data** keeps your currency and your language.

### App lock

Open **⋮ → Settings → General → App access lock** and turn it on. Pondo Flow then asks for
your fingerprint, your face, or the PIN of the device whenever it opens. Turning this switch on
or off asks who you are first, so nobody else can change it behind your back.

When the app is locked you see **Pondo Flow is locked**; tap **Unlock** and confirm. The app
locks itself again a minute after you leave it in the background. If the device has no screen
lock set, Pondo Flow cannot confirm who you are and the app lock cannot be used.

## Categories and the Chart of Accounts

Categories are simply the **Income** and **Expenses** accounts of your chart, so everything
lives in one place. **⋮ → Settings → Books** shows, from the top:

- **Cash, Bank & Cards** — your Cash on Hand and Bank ledgers with their balances, **+ New
  ledger** (up to 2 Cash on Hand and 5 Bank ledgers), your credit cards with **+ New card**
  (see [Credit cards](#credit-cards)) and **Archived ledgers**. Tap a ledger to open it.
- **Chart of Accounts** — tap **Open Chart of Accounts** for the whole chart.
- **Account Types** — the groups of your chart (see [Account Types](#account-types)).
- **Books** (periods) and the **Audit log**.

The Chart of Accounts opens with four summary cards — **Total assets**, **Total
liabilities**, **Total equity** and **Net worth** (*Assets - Liabilities*). Below them are
**Search accounts...** (by name or number), **Filter** and **Add Account**, which creates an
account of any type with an optional subtype. Under the title, **Categories: N of 50** shows
how many categories you use.

The accounts follow in the five standard groups — **Assets**, **Liabilities**, **Equity**,
**Income** and **Expenses** — each with its total; tap a group's header to fold it. Inside a
group, accounts sit under their subtype (such as **Cash and Cash Equivalents**), sorted by
number (1xxx Assets, 2xxx Liabilities, 3xxx Equity, 4xxx Income, 5xxx Expenses). Each account
shows its number, name and balance. When the name needs the room, the amount moves to the
line below it. A parent account folds and unfolds with the arrow at the right end of its row.
The **⋮** next to the title offers **Add the household set**, **Add the organization set**,
**Show disabled & archived**, and **Require fingerprint or PIN to lock / unlock a parent
account** (off by default).

Tap an account to open its sheet: the **Current balance**, its number and **Type**, **Total
debits** and **Total credits**, its **Subtype**, its **Sub-accounts** (tap one to open it), and
its most recent entries. Tap an entry to open it, or **See all** to open **Entries** showing
only this account (a parent includes its sub-accounts); the chip on top of the list removes the
filter. The sheet also holds:

- **Account number** — every number can be changed (digits and dashes, up to 12 characters).
  It must be unique in the book. A new account gets the next free number of its group.
- **Add sub-account** — put accounts under a parent, for example *Wallet* and *Coin bank* under
  *Cash on Hand*. A sub-account gets the parent's number plus *-01*, *-02*… The free version
  allows two levels.
- **Own entries** — a parent that already had entries keeps them. They still count in its total
  and show as a line *"<parent> — own entries"* in the chart and in the reports, until you
  transfer them to a sub-account.
- **Lock this account** — a locked parent takes no new entries, and its own entries cannot be
  moved or corrected. Unlock it to change them. Locking and unlocking are written to the audit
  log.

The default categories can be renamed (each rename is written to the audit log) and disabled,
but not deleted. **Show disabled & archived** lists the ones you turned off. The free version holds up to
**50 categories**, parents included; the core accounts and disabled categories do not count.

### Account Types

**⋮ → Settings → Books → Account Types** shows the five types of your chart and, under each,
its **subtypes** with **Accounts: N**. A subtype is only a heading that groups accounts. You
cannot post to it, it has no balance of its own (its total is the sum of its accounts), and it
does not count toward the 50 categories.

At the top, **These books are for:** **Personal** or **Organization**. The fourth type is
called **Income** in personal books and **Revenue** in an organization's books.

The app starts you with these subtypes:

- **Assets** — **Cash and Cash Equivalents** (your cash on hand and bank ledgers), **Current
  Assets** (amounts owed to you) and **Long-term Assets**.
- **Liabilities** — **Credit Cards**, **Current Payables** (bills you owe) and **Long-term
  Payables**.
- **Equity**, **Income** and **Expenses** start without subtypes; their accounts sit directly
  under the type.

Under any type, **+ Add subtype** creates a new one. Tap a subtype to **Rename** it, **Delete**
it (its accounts stay in the books and become ungrouped under their type) or **Move accounts
here**. An account can move to another subtype of the **same** type, or to **No subtype**, but
never to another type. Your cash, bank, receivable and payable ledgers keep the group the app
gave them; their sheet says so. Every change is written to the audit log.

## Funds and projects

**Funds** are pots of money with a purpose. **Projects** tag spending on a particular event,
renovation, or campaign — a project can draw from any fund.

Open the **Funds** tab to see **All Funds Overview** and every fund as a card. Tap the **New
Fund** button to create one: give it a **Fund Name**, optionally a
**Starting Balance**, a **Purpose or Short Note (Optional)** and a **Target Amount**, and
choose a **Fund Type**:

- **General (Any Purpose)** — everyday money you can spend freely.
- **Set Aside for Purpose** — money reserved for one specific goal.
- **Long-Term / Protected** — a long-term reserve you do not touch.

Some of these labels show your currency in brackets — *Starting Balance (PHP, Optional)*, for
instance — so they look a little different for every user.

Each card shows two numbers. **Available** is the cash the fund holds right now.
**Projected after obligations** is the same money after the bills you still owe and the
amounts owed to you are honoured. Only **Open** bills count, and the projected figure can be
negative — that is a real warning, not a glitch.

Inside a fund you can see its **Money In**, **Money Out**, its **Payables** and its
**Receivables**, and open the entries behind them. **Edit Fund** renames it, changes its
purpose or target, or corrects its starting balance. **Archive** sets a fund aside;
**Un-archive** in **⋮ → Settings → Books → Cash
& Bank → Archived ledgers** brings it back — no money moves, it simply becomes active again.

The **Projects** tab works the same way: **All Projects Overview**, **New Project**, and a
project card showing **Available** and **Projected after obligations**. A project has a
**Default Linked Fund** and an optional **Timeline (Optional)**. When the work is done, open
the project and use **Close Project**; if a balance is left, **Transfer & Close** moves it back
into the fund you pick.

## Entries

An **entry** is one movement of money. On **Home**, tap the round **New entry** button at the
bottom right: the **Quick Entry** dialog opens right there, with four buttons — **Money In**,
**Money Out**, **Card** and **Transfer**. On the **Entries** tab the same button opens the full
entry form, where the modes are called **+ In**, **− Out** and **⇄ Move**. Next to **Filter**
and the download button, **Adjust** corrects the balance of an account (see
[Adjusting a balance](#adjusting-a-balance)).

### Recording money in or out

Fill in the **Amount**, the **Date** (in the form **Use YYYY-MM-DD**), the **Fund**, and the
**Cash Location (Required)** — the cash ledger the money lands in, such as **Cash on Hand** or
a bank account. The cash location is never filled in silently: if there is more than one, you
choose. Add a **Category**, an optional **Project (Optional)**, a **Received From (Payor)** or
**Paid To (Payee)**, and a **Note (Memo)**. Then tap **Save Money In** or **Save Money Out**.

Under **Money Out**, the **Category** list shows your expenses and your liabilities. Pick a
liability — a credit card, for example — to record **Pay a liability**: the cash goes out and
what you owe goes down.

If the amount is more than the fund holds, Pondo Flow warns you with **Not Enough Money in
Fund** and offers **Spend Anyway** or **Change Amount / Fund**.

If you saved twice by accident, the app asks **Possible Duplicate** before the second entry is
written. Every save shows a short message with **Undo**.

### Moving money

**⇄ Move** (or **Transfer** in Quick Entry) offers **Between Funds**, **Between Cash
Accounts** and **Between Accounts**.

- **Between Funds** moves money from one fund to another — pick a **From Fund** and a **To
  Fund**, and the **Cash Account (where the money is)** it is taken from. The money stays in
  your books; only the pot changes.
- **Between Cash Accounts** moves money from one cash ledger to another, such as from your
  wallet to your bank. Pick the **Fund** it is booked to, a **From Cash Account** and a **To
  Cash Account**. The total of the fund does not change; only the cash location does.

- **Between Accounts** moves an amount between two accounts of your chart, and a line under
  the form says what it does — for example *This pays BDO Visa from Cash on Hand*. These moves
  are allowed:
  - between two accounts of the **same type** — always;
  - between an **asset** and a **liability** — paying a card from cash, or a cash advance from
    a card;
  - between a **liability** and **equity**.

  A move between an **asset** and **equity** is not possible: a change to your assets that
  does not touch a liability always shows up in your income or expenses, so record it as
  **Money In**, **Money Out** or an [adjustment](#adjusting-a-balance).

Tap **Save Transfer** when you are done.

### Adjusting a balance

When an account's balance in the app differs from the real one — the cash in your wallet, or a
bank statement — tap **Adjust** on the **Entries** tab. Pick the **Account to Adjust** (its
**Current balance** is shown), then choose how:

- **Set the Balance** — type the **Balance the Account Should Have**; the app posts the
  difference.
- **Add or Subtract** — type the **Amount to Add or Subtract** with **+** or **−**.

**Other Side** decides where the difference goes: **Income / Expense** (the default), or the
**Balance Adjustments** equity account if the difference is a correction rather than real
income or spending. Tap **Save Adjustment**. The adjustment shows in the list like any entry,
and it can be corrected later the same careful way as other entries.

### Correcting an entry

Open an entry to see it in full. From there:

- **Correct** opens the entry for editing: change the **Amount**, the **Date**, the counterparty,
  the **Note**, the **Memo** or the **Cash Location**, give a **Reason**, and tap **Save
  Changes**. Pondo Flow then writes the correction the careful way — the original is voided, a
  reversal is posted, and the replacement is recorded in one go, so the history of the entry
  stays intact. The **Reason** is kept in the audit log.
- **Void** cancels the entry and posts a reversal, so the money comes back. The entry stays in
  the journal, marked as voided. A **Reason** is required here too.

A deactivated entry can be brought back from the **Audit Log**, or by undoing the void.

### Receipt photos

Attach a photo of a paper receipt to any entry. Open the entry and tap **Add receipt photo**,
then choose **Camera** to take one or **Gallery** to pick an existing photo. An entry can hold
up to five receipt photos. Tapping a photo opens it full screen; **Delete photo** removes it
from the entry.

Each photo is made smaller, stripped of the details that say where and when it was taken, and
kept encrypted on the phone. **Export backup** carries the photos along (see
[Backup and restore](#backup-and-restore)).

## Credit cards

Pondo Flow treats a credit card as what it is in your books: money you owe (a **liability**).
A purchase on the card adds to what you owe; paying the card takes cash out and brings what
you owe down.

**Adding a card.** Open **⋮ → Settings → Books → Cash, Bank & Cards** and tap **+ New card**.
Give it a **Card name** (for example *BDO Visa*), and optionally a credit limit and the last
four digits, shown as **•••• 1234**. You can hold up to 5 cards (**Credit cards (N of 5)**);
they do not count toward the 50 categories. Every card sits in the **Credit Cards** subtype of
your Liabilities.

**Spending with a card.** On **Home**, open **Quick Entry** and choose **Card**. Pick the
**Credit card**, choose **Purchase** or **Refund**, then fill in the amount, the category and
a note. A purchase counts in your budgets when you make it, not when you pay the card.

**Paying a card.** Tap **Pay card** next to the card (in **Cash, Bank & Cards**). It opens
**Money Out** with **Pay a liability** and the card already chosen; enter the amount and the
cash ledger it comes from. You can also move the money with **⇄ Move → Between Accounts**.

**Seeing your cards.**

- **Home** shows the **Credit cards** tile next to your cash. Tap a card to see its entries.
- **Reports → Credit cards** shows each card's **Opening balance**, **Spent on cards**,
  **Card payments** and **Closing balance**, with **Available** when it has a limit.
- **Cash Coverage** counts what you owe on your cards. The cash-flow figures do not, because a
  card purchase moves no cash until you pay it.

## Bills to pay and to collect

Open **⋮ → Bills to Pay** for the money you owe, and **⋮ → To Collect** for the money owed to
you. Tap **+** to add one.

For a bill, give a **Payee / Biller**, an **Amount**, a **Due Date**, a **Fund**, a **Category**,
an optional **Project (Optional)** and a **Memo (Optional)**. For an amount to collect, the
counterparty is **From Who**. Tap **Save Bill** or **Save**.

Each list has filters: **All**, **Unpaid**, **Overdue**, **Paid** (or **Collected**). A bill
shows its **Due** date and a status of **UNPAID**, **OVERDUE**, **PAID** or **CANCELLED**.

To settle one, open it and tap **Mark Paid** or **Mark Received**. Pondo Flow fills in the
entry for you; you confirm the cash location it is paid from. If the fund does not hold enough,
you are asked **Pay Anyway** or you cancel.

### Repeating bills and expected receipts

A bill that repeats is still a bill — you set the rule on it, and the app creates the next one
for you. Open the bill, tap **Repeat**, and choose **Never**, **Weekly**, **Every 2 weeks**,
**Monthly**, **Quarterly** or **Yearly**. Under **Ends** you can pick **Never**, **On a date**
or **After a number of times**. The same choices are on an amount to collect.

A repeating bill needs a payee and a due date, and a repeating collection needs a payee and a
due date too. Without one, Pondo Flow asks you to add it or turn the repeat off.

Entries repeat the same way: set **Repeat** on an entry to make it repeat. The rules live in
**⋮ → Repeating entries** (on the **Entries** tab), where you can **Pause**, **Resume**,
**Edit** or **Delete** each one. A rule that was set to **Ask me first** waits for you in the
**Action Queue** on **Home**, where you **Post** it or **Skip** it.

## Budgets

Open **⋮ → Budgets**. At the top of the screen is the card **New Budget (Fund · Project ·
Category · Period)**.

Fill in the **Budget Amount**, then choose the **Fund:**, the **Project (Optional):** — pick
**Whole Fund** to budget the fund as a whole — and the **Expense Category:**. Under **Period:**
choose **This Month**, **This Quarter**, **Year to Date** or **Custom**; a custom period asks
for a **Start (YYYY-MM-DD)** and an **End (YYYY-MM-DD)**. Tap **Save Budget**.

Each budget line shows **Budget:**, **Actual:** and **Var:** — the difference between the two.
A note appears when project spending is detected on another fund, so you are not surprised by a
number that does not add up.

## Reports

Open the **Reports** tab. The title of the page is **Reports & Summary**, and it is a carousel:
swipe left and right to move between the report pages, and the page indicator shows where you
are. The name of the report you are on is written above the pages — tap it to open **Choose a
report** and jump straight to one.

The report pages are:

- **Summary** — **Income & Spending Summary**: **Total Income**, **Total Spending** and **Net
  Saved / Spent**, with **Cash in**, **Cash out** and **Ending Balance** on top.
- **Position** — **Statement of Financial Position**: **Assets**, **Liabilities** and **Net
  Assets**, as of a date.
- **Budget** — **Budget vs Actual**: budget against what was actually spent.
- **Charts** — **Monthly income and spending**, **Income by account** and **Spending by
  account**.
- **Credit cards** — the book balance of every card, its spending and its payments.

Use **Filters** to set the **Date Range:**, the **Fund:** and the **Project:**. **Hide** closes
the filters again.

### Tap an amount

Every amount on a report is a tap target. Tap one and a popup opens showing the entries behind
that exact amount, with its **Total** at the bottom. From there you can **View in Entries** to
see them in the list, or **View in Payables** for an amount that comes from unpaid bills. If
nothing sits behind the amount, the popup says so.

### The project statement

Open the **Projects** tab and tap a project. You get its **Project statement**: the whole life
of the project by default, or the period you choose. It shows **Money in by source**, **Money
out by category** and the **Balance** — what the project carried in, what it holds, its
**Payables** and **Receivables**, and the **Projected after obligations** figure.

Every amount in the statement is a tap target too. A closed project keeps its statement and
says it is read-only.

To keep a copy, use **Export CSV** on the report, or **Share reports**.

## Contacts

Open **⋮ → Contacts**. The list shows the people and businesses you deal with, and searches by
name, phone, or email. Tap **+** for **New Contact**.

A contact has a **Name**, and optionally a **Phone (Optional)**, an **Email (Optional)**,
**Notes (Optional)** and an **Add photo** button. The **Type** is one of **Unclassified**,
**Vendor**, **Customer**, **Friend**, **Donor** or **Family**; you can add your own types under
**Contact types**.

Contacts are suggested automatically when you type a payee or a customer name in an entry, so
you rarely enter the same person twice.

Open a contact to see the **Linked entries** — every entry ever recorded with that name,
across funds and projects — and its change history. **Protect** locks the contact: it cannot be
renamed or deactivated, and its entries cannot be edited or voided. **Unprotect** asks you to
confirm who you are first.

To take a copy of the list, tap **Export** and choose a **PDF Document**, a **CSV File** or an
**Excel Workbook**.

## Backup and restore

Open **⋮ → Settings → Backup**. Two cards do the work.

### Export & Import (Data Portability)

- **Export backup** writes one ZIP with your whole database **and your receipt photos**. Before
  it saves, it tells you how many photos it carries and how big the file is (for example
  "12 photos, 4.1 MB").
- **Import backup** reads such a ZIP back in, photos included — so a restore on a new phone
  brings the pictures back too. A backup is restored completely or not at all.
- **Export JSON** writes your database (without the photos) to a single file.
- **Export CSVs (.zip)** writes the tables as a zipped set of CSV files.
- **Import JSON Backup** reads a JSON backup back in.

Keep backup files private: anyone who has the file can open your books **and** the photos in it.

Android's own file picker asks where to save and which file to open, so you choose the place.
A restore **replaces** your current data — Pondo Flow asks you to confirm first, and offers to
export the current books before you do.

### Auto-Backup (Safety Net)

**Automatic snapshots** is off until you turn it on. When it is on, tap **Choose Folder** and
pick a place you control, such as a subfolder of Downloads or in Google Drive. Pondo Flow then
writes a plain-text snapshot when the app opens and once a day. The app never puts anything in
a shared folder on its own.

- **Back Up Now** writes a snapshot right away.
- **Restore Latest** reads the newest snapshot back from the folder.
- **Change Folder** points the snapshots somewhere else.

After you reinstall the app, pick the same folder again and restore from it. The database on
the phone is encrypted, so the backup file is the one plain copy — keep it somewhere safe.

## Audit log and closing a period

### Audit Log

Open **⋮ → Audit Log**. It lists every change Pondo Flow recorded, newest first, and it is
append-only — it is never rewritten. Filter it with **All** or **Deactivated**. Rows show
actions such as **Created**, **Edited**, **Deactivated**, **Restored**, **Period closed** and
**Period unlocked**, on records such as **Entry**, **Contact**, **Cash ledger**, **Bill**,
**Collection**, **Budget**, **Fund**, **Project** and **Period**. On a deactivated record you
can tap **Restore** to bring it back.

### Closing a period

Open **⋮ → Settings → Books**, card **Books**. Under **Period scheme** you can use a **Calendar
year** or a **Custom fiscal year**. The card shows the **Current period**.

Tap **Close this period** (or **Close the previous period**, which names the dates it covers)
to lock a period. Closing
locks every entry and every audit row of that period, so mistakes cannot be edited quietly
later. Corrections to a closed period are posted as new entries in the current period. A closed
period can be **unlocked** later — the app asks you to confirm who you are, and every close,
unlock and edit is written to the audit log. Closed periods are listed under **Closed
periods**.

## Privacy mode

Open **⋮ → Settings → General → Device & Privacy** and turn on **Privacy mode**. Screenshots
and the preview in the recents are blocked, so your books never leave the app by accident.

While the app lock is on, privacy mode cannot be turned off — the app lock already keeps the
window secure.

## About, privacy and support

Open **⋮ → Settings → About → About Pondo Flow**:

- **Privacy policy** and **Terms of use** open inside the app — they work without internet.
- **Contact support** opens your email app with a message to **support@sigbin.net**, with the
  app and Android version filled in (never your books). If no email app is installed, the address
  is shown so you can copy it.

Found a bug or have an idea? [Open an issue](https://github.com/jhassuni/pondoflow/issues/new/choose).

## Languages

Open **⋮ → Settings → General → Language** and tap a language: the app switches at once.
**More languages…** lists them all. The app ships in these languages:

| Language | Status |
| --- | --- |
| English | Current |
| Español | Shipped |
| Français | Shipped |
| Português (Brasil) | Shipped |
| العربية | Shipped |
| Kiswahili | Beta / Community Translated |
| हिन्दी | Beta / Community Translated |
| বাংলা | Beta / Community Translated |
| Bahasa Indonesia | Beta / Community Translated |
| Русский | Beta / Community Translated |

The language in use is marked **Current**. The five community translations are marked **Beta /
Community Translated** because they were translated by the community and may still be being
improved.
