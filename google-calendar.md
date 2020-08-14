## Control which Google Account links affect

If you're logged in with multiple Google Accounts in your browser, clicking a link to for example add an event to your calendar will try to add this event to the calendar of your default Google Account (the one you've logged in with first). To control which Google Account to use, you can modify the link. Example:

- Original link: `https://calendar.google.com/event?action=TEMPLATE&tmeid=xxx&tmsrc=yyy%40group.calendar.google.com`
- Modified link: `https://calendar.google.com/b/2/event?action=TEMPLATE&tmeid=xxx&tmsrc=yyy%40group.calendar.google.com`

Notice the added `b/2/`. Here `2` referes to the 3rd logged in Google Account (the list is zero-indexed)
