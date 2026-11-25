# Job application tracker

Keep one Excel row per job application. A scheduled Codex chat checks Gmail for confirmations and employer replies, updates the workbook, and writes a short daily summary. An iPhone Shortcut sends that summary to a chosen WhatsApp contact.

## Set up your tracker

1. Connect your Gmail account in Codex. Use a local Codex chat on a Mac with access to your files.
2. Copy [the blank workbook](templates/job-applications.xlsx) to a private folder outside the repository. Use this working copy for applications and email links.
3. Create a **Job Updates** folder in iCloud Drive. Confirm that the same folder appears in Files on your iPhone.
4. Copy the [automation prompt](automation.md) into your tracker chat. Fill in your working workbook path, iCloud folder path, time zone, and the date you want the first Gmail search to start. Check the first import and confirm the recurring schedule is active.
5. Follow the [iPhone setup](iphone-shortcut.md). The example schedule prepares the message at 8:30 PM and sends it at 9:00 PM New Zealand time. Allow the Mac to run the scheduled task and sync the file before delivery.

## Use it day to day

Tell the tracker chat “I applied for the Support Analyst role at Example Company today,” or enter the company, role, date, and status in the first empty row of the **Applications** table. Use **Awaiting response** for a new application. The next matching confirmation or reply updates that row. Filter **Status** to see rejections, interviews, or offers.

The **Needs review** tab holds messages that need your judgment. If two roles at the same company could match a reply, identify the correct role in the tracker chat. When a date is unknown, leave it blank.

The dated text file contains only the message for the recipient. The workbook and review questions stay private. The daily cleanup keeps seven calendar days of drafts.

## Put this template on GitHub

Create a repository named `job-application-tracker` and upload the contents of this folder at its root, including the `templates` directory. Keep the workbook in that directory blank when sharing the project.
