---
name: content-calendar
description: Use when someone wants a content calendar, posting plan, or social media schedule for their business or personal brand — interviews them briefly, then builds a real calendar they can use: a dated plan table, a CSV for Google Sheets / Notion / Excel, and an .ics file that drops every post into Google Calendar, Outlook, or Apple Calendar.
---

# Content Calendar

Turn "I should post more consistently" into a real calendar that sits in the user's own tools, with dates, reminders and something specific to post every time.

## Step 1: Ask a few questions (one message, skip any already answered)

1. **What do you sell, and who to?** (one sentence)
2. **Where do you post?** (e.g. Instagram, TikTok, Facebook, LinkedIn, Threads, newsletter, WhatsApp channel)
3. **How often can you realistically post?** Use their real number, not an ideal one.
4. **Start date and how many weeks?** (default: 4 weeks from next Monday)
5. **Anything already happening?** Launches, promos, holidays, events.
6. **Goal for this period?** (enquiries, bookings, followers, sales of one product)

If they're unsure about frequency, suggest 3 posts a week. That's sustainable for a solo owner.

## Step 2: Plan

- Pick **one theme per week** that serves the goal, and build that week's posts around it.
- Rotate post types so the feed isn't all selling:
  - **Teach**: a tip, myth or how-to
  - **Show**: behind the scenes, process, results
  - **Prove**: a review, testimonial or before/after (only real ones; never invent)
  - **Ask**: a question or poll that's easy to answer in one line
  - **Offer**: a clear call to action (book, DM, WhatsApp, buy)
- Aim for roughly 1 offer post for every 3–4 others.
- Put real dates and holidays in the plan (check the user's country), and add launch or promo dates the user gave.
- Each post needs a **hook** (first line) and a **CTA**, not just a topic.

## Step 3: Deliver three things

**1. The calendar table** (shown in chat)

| Date | Day | Platform | Type | Topic | Hook (first line) | CTA | Status |
|---|---|---|---|---|---|---|---|

Set Status to `Idea` for every row. Suggested flow: Idea → Drafting → Scheduled → Posted.

**2. `content-calendar.csv`**: the same columns. Use ISO dates (`2026-12-07`) and quote every field, so it imports cleanly into Google Sheets, Notion or Excel.

**3. `content-calendar.ics`**: one all-day event per post, so the plan shows up in their calendar app:

```
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//content-calendar-skill//EN
CALSCALE:GREGORIAN
X-WR-CALNAME:Content
BEGIN:VEVENT
UID:<date>-<n>@content-calendar
DTSTAMP:<now in UTC, e.g. 20261118T090000Z>
DTSTART;VALUE=DATE:<yyyymmdd>
DTEND;VALUE=DATE:<yyyymmdd + 1 day>
SUMMARY:[<Platform>] <Topic>
DESCRIPTION:Hook: <hook>\nCTA: <cta>\nType: <type>
BEGIN:VALARM
TRIGGER:-PT6H
ACTION:DISPLAY
DESCRIPTION:Post tomorrow: <topic>
END:VALARM
END:VEVENT
END:VCALENDAR
```

- Escape backslashes, commas, semicolons and newlines in text fields (`\\` `\,` `\;` `\n`).
- Every line ends with CRLF, including the last one.
- Fold any line longer than 75 bytes: break it and start the continuation line with a single space. Never split an emoji or other multi-byte character.
- Every event needs a unique UID.
- The alarm counts back from midnight at the start of the post day, so `-PT6H` fires at 6pm the evening before. That gives the user time to prepare. Apple Calendar and Outlook honour it. Google Calendar ignores reminders in imported files and uses the calendar's default notification instead, so say this in Step 4.
- If you write the CSV with code, start it with a UTF-8 BOM so Excel shows accents and emoji correctly.

If you can write files, save both files and tell the user where they are. If you can't, give each one in its own code block and tell the user to save it with that exact filename.

## Step 4: Tell them how to use it

End with 3 short lines:
- **Google Calendar:** Settings → Import & export → Import → choose `content-calendar.ics`. Tip: import into a new calendar called "Content" so it's easy to hide or delete. To get reminders, set that calendar's default notification (Settings → the calendar → Event notifications), because Google skips reminders in imported files.
- **Google Sheets / Notion:** import `content-calendar.csv`.
- **Each week:** move rows from Idea to Drafting on Monday, and batch-write that week's posts in one sitting.

## Rules

- Keep it realistic. A plan the user can't keep up with is worse than a smaller one.
- Never invent testimonials, statistics or reviews. For "Prove" posts, write a prompt such as "Share a recent client message (with permission)".
- Write hooks in the user's language and tone. If they write casually, keep it casual.
