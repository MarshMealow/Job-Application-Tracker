# Daily automation prompt

Copy the text below into a local Codex chat after filling in the four bracketed values. The first-run date controls the historical import.

---

Set up my job tracker in this chat. Run the first import now, then refresh it daily at 8:30 PM in [time zone, e.g. Pacific/Auckland]. Use my connected Gmail, my manual additions in this chat, the private Excel workbook at [workbook path], and the iCloud Drive draft folder at [folder path].

**Find applications and outcomes.** For the first import, search from [first-run date]. On later runs, search from the last successful sync with a two-day overlap. Paginate results and read relevant messages, including confirmations from job platforms and replies directly from employers. Skip ads, suggested jobs and reminders to finish an application.

**Update Excel.** Add one row per application to the Applications table. For manual entries, capture company, role, application date when known, and status. Match Gmail evidence using the role, company, requisition, dates and source links. Merge a confirmation with an existing manual entry when the match is clear. Preserve repeat applications, user corrections, unrelated rows, table layout and date formats. Store source links in Application email and Status email. Set Status date from the evidence. If a message could refer to multiple jobs, record it once in Needs review with its date, subject, reason and Gmail link.

Use Awaiting response for a receipt, Interview for an invitation, Offer for a written offer and Accepted when I confirm acceptance. Use Rejected for a clear rejection. Keep an expired listing or silence from changing the status. A platform prediction that a job is unlikely to progress can be recorded as Unlikely to progress. A later generic receipt or platform notice must preserve a confirmed decision.

**Save and verify.** Work on a temporary copy of the current workbook. Verify the edited rows, check that the original is available and unchanged since reading, then replace it. If the workbook is locked or access fails, report the issue here and retain the previous successful sync point. Reprocessing a message must preserve the same application and outcome.

**Prepare the daily message.** Summarize new applications and confirmed developments since the previous successful report in a short first-person message for my chosen recipient. Include manual applications. On the first run, count only today's events as today's activity. A quiet day gets a short no-change message. Keep Gmail links and review questions in the tracker chat. Write the message as UTF-8 plain text named `yyyy-MM-dd.txt` using the report's local date. Publish it atomically after verifying the sync and confirm the saved text. The iPhone handles delivery. Report failures in this chat.

**Clean up.** After verifying today's file, keep today and the preceding six calendar dates. Delete only older regular files directly in the draft folder whose complete name is a valid date followed by `.txt` in that exact format. Skip symlinks, folders, future dates and other filenames.
