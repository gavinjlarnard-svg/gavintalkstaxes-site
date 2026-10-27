---
layout: default
title: "Tax Organizer privacy policy"
permalink: /tax-organizer/privacy/
---

# Privacy policy

**Product:** GavinTalksTaxes Tax Organizer
**Publisher:** Gavin Larnard (GavinTalksTaxes)
**Effective date:** October 27, 2026
**Contact:** gavin@seniortaxpro.com

## The short version

- Tax Organizer is a Chrome extension. It runs on your computer.
- We do not run a server for Tax Organizer. We never receive your tax data, your email, or your files.
- Your data is saved on your computer, encrypted with a passphrase only you know.
- Tax Organizer reads your Gmail only if you connect it, and it can only read. It cannot send, delete, or change email.
- We do not sell your data. We do not show ads. We do not use analytics or tracking.
- You can delete everything at any time from **Settings → Delete all my data**.

Tax Organizer does not file your taxes and does not give tax advice. It helps you gather your documents and shows you what to look at.

## Who "we" are

"We" means the publisher named above. The publisher is the only party that builds and updates Tax Organizer.

## What Tax Organizer stores, and where

Everything Tax Organizer saves stays in your Chrome profile on your computer. It is not synced to other devices and not sent to us.

### Saved and encrypted (in Chrome's extension storage on your computer)

When you first open Tax Organizer, you create a passphrase. Tax Organizer turns that passphrase into an encryption key. It uses that key to encrypt everything below before saving it.

- **Your profile answers.** For example filing status, age group, and your answers to the short questions.
- **Facts read from last year's tax return**, if you choose to load it. Only the amounts and names the app needs are kept.
- **Facts read from each tax document you import.** For example the form type, the tax year, the payer's name and ID number, the amounts in each box, and a fingerprint of the file (a SHA-256 hash) used to spot duplicates.
- **Email scan results.** For each possible tax email: the sender, subject, date and attachment names. Not the message text.
- **Payroll-page scan results.** The names and addresses of the document links Tax Organizer found on the page.
- **An activity log** of what you did in the app (for example "Imported a 1099-INT"). You can see it under **Settings → Activity log**.
- **An error log**, only if you turn it on. It is off by default.

About ID numbers on your forms: Tax Organizer keeps the payer's ID number (a business number) from your forms. For your own Social Security number, it keeps only the last four digits, even when a form prints the full number. The last four digits help tell your forms apart from a spouse's.

Tax Organizer does **not** keep a copy of your PDF files. It reads them, keeps the facts listed above, and lets the file go.

### How the encryption works

- Encryption: AES-GCM with a 256-bit key.
- Key: made from your passphrase with PBKDF2-SHA-256, 600,000 rounds, and a random salt.
- Your passphrase is never saved and never sent anywhere.
- The key exists only in memory while Tax Organizer is open and unlocked.
- Tax Organizer locks itself after 30 minutes without activity.
- If you forget your passphrase, we cannot recover your data. Nobody can. You would need to delete it and start over.

### Kept briefly in memory (not encrypted with your passphrase)

Chrome's "session" storage is kept in memory and is cleared when Chrome closes. Tax Organizer uses it for two things only:

- **The printable summary.** When you open it, your summary data is passed to the summary tab through session storage. The summary tab removes it as soon as it loads. Locking Tax Organizer also clears it.
- **Outlook sign-in tokens**, if you connect Outlook. These are cleared when you disconnect, erase your data, or close Chrome.

Gmail sign-in tokens are managed by Chrome itself (through Chrome's built-in identity feature), not stored by Tax Organizer.

### Files you choose to save

Some actions save a normal, unencrypted file on your computer. They happen only when you click them:

- **Save a copy to Downloads** when importing from a payroll site saves that PDF to your Downloads folder.
- **Print or save the summary** creates whatever file or printout you choose.
- **Export the error log** saves a file with the error entries.

These files are yours. Tax Organizer does not track or delete them.

## What Tax Organizer connects to on the internet

Tax Organizer has no server of ours to talk to. It connects only to the services you choose, only when you take an action, and only to read.

| Service | When | Why |
| --- | --- | --- |
| Google sign-in (handled by Chrome) | When you click **Scan my email** with Gmail | To ask your permission for read-only Gmail access. |
| `gmail.googleapis.com` (Gmail API) | When you scan your email or import an attachment | To search for tax-form emails, read their sender, subject, date and attachment names, and download the attachments you tick. |
| `oauth2.googleapis.com` | When you click **Disconnect email** | To cancel Tax Organizer's Gmail access with Google. |
| `login.microsoftonline.com` | Only if you connect Outlook | To sign in to Microsoft and get read-only mail access. |
| `graph.microsoft.com` (Microsoft Graph) | Only if you connect Outlook | Same as Gmail: search, read sender/subject/date/attachment names, download the attachments you tick. |
| Your payroll or HR website (for example ADP, Workday, Gusto) | Only when you are on that site, signed in, and click **Scan this page** and then **Import selected** | To list document links on that page and download the ones you tick, from that same website. |

Chrome asks you to approve access to each of these before Tax Organizer can use it.

Tax Organizer also shows links to irs.gov and other official pages. Those open in a normal browser tab only when you click them.

Tax Organizer does **not**:

- send anything to us or to any server we run,
- use analytics, crash reporting, or tracking of any kind,
- load code from the internet (all code ships inside the extension),
- use AI services or send your data to any third party for processing,
- read your email or web pages in the background.

**Demo mode** uses fake sample data bundled in the extension. It makes no network connections.

## Gmail: exactly what we use and why

If you connect Gmail, Tax Organizer asks Google for the permission called `gmail.readonly`. This permission can read but cannot send, delete, label, or change email.

What Tax Organizer does with it:

1. Runs a few searches for tax-form emails in the tax-year window (for example, emails with W-2 or 1099 in the subject, or from known payroll and brokerage senders).
2. For each match, reads only these parts: **From, Subject, Date, List-Unsubscribe**, and the **names and sizes of attachments**. It does not read the message text.
3. Shows you the list. Emails that look like scams are flagged and not imported.
4. Downloads an attachment **only when you tick it** and click import. The PDF is read on your computer. Only the facts listed above are kept.

**Google API Services User Data Policy.** Tax Organizer's use and transfer to any other app of information received from Google APIs will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

In plain terms:

- **Use.** Gmail data is used only to find and read your tax forms and show them to you in Tax Organizer. Nothing else.
- **No transfer.** Gmail data is not sent to us or to anyone else. It stays on your computer.
- **No humans.** No person reads your Gmail data. We cannot, because it never reaches us.
- **No ads.** Gmail data is never used for advertising, never sold, and never used to judge credit or lending.
- **No AI training.** Gmail data is not used to train any AI or machine-learning model.

To stop Gmail access: click **Disconnect email** in Tax Organizer. That cancels the access with Google. You can also remove Tax Organizer at <https://myaccount.google.com/permissions>.

## Outlook

Outlook is not available yet. Tax Organizer does not connect to Microsoft accounts today. When Outlook support is added, this section will apply and we will update the date at the top:

If you connect Outlook, Tax Organizer asks Microsoft for `Mail.Read` (read-only mail access), plus `openid` and `offline_access` so you stay signed in during your session. It uses this the same way as Gmail: search, read sender, subject, date and attachment names, and download only the attachments you tick. **Disconnect email** forgets the Outlook sign-in on your computer. To fully remove access, remove the app in your Microsoft account (personal: <https://account.microsoft.com/privacy/app-access>; work or school: <https://myapps.microsoft.com>).

## Payroll and HR websites

- You sign in to your payroll site yourself, in your own tab. Tax Organizer never sees or stores your password.
- Tax Organizer reads the page only when you click **Scan this page**.
- It reads link names and addresses. It never types, clicks buttons, submits forms, or changes settings. It skips any form with a password field.
- It downloads only the files you tick, and only from the same website.

## Sharing and selling

We do not sell, rent, share, or trade your data. We cannot, because we never receive it.

The services you connect (Google, Microsoft, your payroll provider) have their own privacy policies. Tax Organizer does not change what they collect.

The Chrome Web Store, run by Google, gives publishers general statistics such as the number of installs. That data comes from Google, not from Tax Organizer. The website where this policy is posted (gavintalkstaxes.com) is hosted on GitHub Pages. GitHub may log visitors' IP addresses for security, under GitHub's own privacy statement. The site itself sets no cookies and has no analytics, and neither does the extension.

## Deleting your data

- **Delete everything:** Settings → **Delete all my data**. This erases the encrypted data and memory-only data on this computer and signs out of email.
- **Forgot your passphrase:** on the lock screen, choose **Erase everything and start over**.
- **Uninstall:** removing the extension makes Chrome delete its stored data.
- **Email access:** **Disconnect email**, plus the Google or Microsoft links above.
- Files you saved yourself (Downloads, printouts, exports) are not deleted by Tax Organizer. Delete them like any other file.

Because we never hold your data, there is nothing for us to delete on our side. You do not need to ask us.

## Security

- Data is encrypted on your computer as described above.
- A strict content security policy blocks code from the internet.
- Text from emails, web pages and PDFs is treated as plain data. Tax Organizer never follows instructions found inside them.
- Limits: if someone can use your computer while Tax Organizer is unlocked, or if your computer has malware, encryption cannot fully protect you. Use a strong passphrase that you do not use anywhere else, and lock Tax Organizer when you step away.

## Children

Tax Organizer is for adults who file their own taxes. It is not meant for children under 13, and we do not knowingly collect data from anyone.

## Not tax advice

Tax Organizer shows possible deductions and where amounts usually go on a return. These are suggestions to check, not tax, legal or financial advice. You are responsible for your return.

## Changes to this policy

If we change this policy, we will update the date at the top and describe the change in the extension's release notes. If a change would send data off your computer, we will ask for your permission in the extension first.

## Contact

Questions about this policy or your data: gavin@seniortaxpro.com
