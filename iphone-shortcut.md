# Send the daily update from iPhone

Use the same iCloud Drive folder and local calendar date as the Mac. Start after the tracker has created today's dated file.

1. In **Files → Browse → iCloud Drive → Job Updates**, open today's file and check the text.
2. In **Shortcuts → Automation**, create a **Time of Day** automation. Choose **9:00 PM**, **Daily**, and **Run Immediately**. The trigger follows the iPhone's local time.
3. Add **Format Date**. Select the built-in **Current Date** variable as its input. Expand the action and choose **Custom** with format string `yyyy-MM-dd`.
4. Add **Get File from Folder** and select **Job Updates** in iCloud Drive. In the path field insert the **Formatted Date** variable, then type `.txt` immediately after it. For example, 25 November 2026 resolves to `2026-11-25.txt`. Enable **Error If Not Found** so the run stops if today's draft is missing.
5. Add **Get Text from Input** below the file action. Add **Quick Look**, then tap **▶**. Check that the preview shows the actual update.
6. Replace **Quick Look** with the WhatsApp **Send Message** action. Select the **Text** output as its message and choose yourself as the test recipient. Tap **▶** to send the test. For a locked-phone test, temporarily set the trigger a few minutes ahead, lock the phone and check your self-chat afterward.
7. After the test succeeds, restore **9:00 PM** and select the intended recipient. A manual run now sends to that contact immediately.

If the error mentions a file called only `.txt`, preview the output of **Format Date** and check the variable in the path. If the error contains the correct date, check whether today's file has reached the iPhone in Files.
