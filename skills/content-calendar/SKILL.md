---
name: content-calendar
description: Use when an SME, startup, or personal brand wants a content calendar, posting plan, or social media schedule — diagnoses their business stage and where their funnel leaks, sets a funnel-weighted content mix, gives every post a storytelling format, and delivers a real calendar: a dated plan, a CSV for Sheets/Notion/Excel, and an .ics file for Google Calendar, Outlook, or Apple Calendar.
---

# Content Calendar

Most content calendars plan posts. This one first works out **what the business actually needs from its content**, then plans posts that do that job. The output lives in the user's own tools.

The flow: **Interview → Diagnose → Set the mix → Plan with stories → Deliver files → Review in 4 weeks.**

## Step 1: Interview (one message, skip anything already answered)

Ask these in plain language, as one short numbered list:

1. **What do you sell, to whom, and roughly what does it cost?**
2. **Where are you right now?** (not launched yet / have first customers / steady sales, want more / established with loyal customers)
3. **Your numbers, roughly. Guesses are fine:** typical views per post, enquiries (DMs/WhatsApp/calls) per week, how many enquiries become customers, and how many customers come back.
4. **What are the top 3 questions or doubts customers ask before buying?**
5. **Where do you post, and how many posts a week can you make in total?** If they use more than one platform, ask whether they cross-post the same content or make separate posts.
6. **Start date and number of weeks (default 4).**
7. **Anything coming up in that time?** Launches, offers (with the real price, cut-off date and who it's for), events, and days you're closed.

If they have no numbers, accept answers like "lots of views, hardly any DMs". Those are enough to diagnose.

## Step 2: Diagnose

Read [references/stages-and-leaks.md](references/stages-and-leaks.md). Decide:

- **Stage:** Pre-launch, Early traction, Growth or Established
- **Main leak:** Not seen, Not trusted, Not buying or Not returning
- **Goal for the period:** one sentence with one target that can move **within this period**. Size the target from the user's own numbers, following the guide in stages-and-leaks.md.

If stage and leak point different ways, **the leak wins**. If the period crosses a launch date, use the Pre-launch mix before launch and the Early traction mix after. Apply the same leak adjustment to both parts, and count launch day as "after".

If a number you need to size the goal is missing (e.g. how many people are already on the waitlist), ask one short follow-up question. If you can't ask, state your assumption in the goal line.

Show the diagnosis in a short box before the plan, with the goal as its last line:

> **Diagnosis:** You're at *Early traction*. Your main leak is *Not buying*: people DM to ask about price but few book. So this month leans on proof and objection-busting posts, not reach.
> **Goal:** Move enquiry-to-booking from about 2 in 10 to 3 in 10 by the end of the month.

## Step 3: Set the content mix

Read [references/funnel-mix.md](references/funnel-mix.md). Apply the base mix for the stage, then the leak adjustment, then turn it into whole post counts using the rounding rule there. **The post counts must add up to the total number of posts.**

Then pick **3–4 content pillars**: recurring themes drawn from what they sell and what customers care about.

## Step 4: Plan the posts

Read [references/story-formats.md](references/story-formats.md). For every post, assign a **funnel stage** (from the counts in Step 3), a **pillar** and a **story format** suited to that stage. Then write:

- the **hook** (first line)
- a one-line **story beat outline** (Hook → Tension → Turn → Lesson/Proof → CTA)
- the **CTA**
- **one success metric** matching the funnel stage

### Rule priority: when rules clash, the higher rule wins

1. **The mix from Step 3 is the budget.** Every rule below works inside those counts and never changes them.
2. **Customer questions (Q4):** put each one in a Conversion post (FAQ answer or Objection buster). If there are more questions than Conversion posts, answer the rest in Consideration posts ("How we do it", "Problem–Agitate–Solve"), or combine two questions in one post.
3. **Launches and offers get a campaign arc.** Each arc step has a fixed funnel stage (see story-formats.md), and every arc post counts against that stage's budget. An arc step may use any format of its funnel stage, so an Offer can also answer a customer question. If the budget is too small for the full arc, drop steps in this order: Recap, Proof, Tease.
4. **Spacing:** never put two Conversion posts next to each other. Any non-Conversion post between them is fine. Don't use the same story format twice in a row.
5. **Calendar advice** (payday, year-end leave, festive timing) decides *where* posts go, never *how many* of each stage.

### Facts and honesty

- **Never invent testimonials, reviews, numbers or product facts.** Where a post needs a fact the user didn't give (shelf life, process steps, a customer quote, a real result), write a placeholder in square brackets, e.g. `[your steep time]` or `[customer message, with permission]`.
- Hooks use only facts the user gave. The examples in story-formats.md are illustrations, not facts to copy. Formats that need a personal belief or moment ("I used to think…", Founder story) get a placeholder for it, e.g. `I used to think [old belief].`
- If a format assumes something the business doesn't do yet (a reminder service, a members' perk), mark the post **"(set up first)"** in its topic, so the user knows to set it up or swap the post.

### Dates

- **Default posting days:** spread posts evenly across the week (3 posts → Mon / Wed / Fri; 4 → Mon / Tue / Thu / Sat; 5 → weekdays).
- Move a post off a day the user is closed, and off national holidays where the audience is offline. Move it to the nearest open weekday, earlier rather than later. Keep a post on a state holiday unless most of the audience is in that state.
- Check [references/sea-calendar.md](references/sea-calendar.md) for the user's country and **confirm exact dates for the plan's year** with a search when you can. If sources disagree on a date, avoid relying on that day and tell the user which date to double-check.
- **Cross-posting:** one row per post, with Platform listing all platforms (e.g. "Instagram + TikTok"). If the user makes separate posts for each platform, make one row per platform post.

## Step 5: Deliver three things

**1. The diagnosis box and calendar table** (in chat)

| Date | Day | Platform | Funnel stage | Pillar | Story format | Topic | Hook | Story beats | CTA | Success metric | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|

- Set Status to `Idea` for every row. The flow is Idea → Drafting → Scheduled → Posted.
- For campaign arc posts, add the arc step in brackets after the format, e.g. `Objection buster (Offer)`.

**2. `content-calendar.csv`**: the same columns. Use ISO dates (`2026-12-07`), quote every field and start the file with a UTF-8 BOM.

**3. `content-calendar.ics`**: one all-day event per post:

```
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//content-calendar-skill//EN
CALSCALE:GREGORIAN
X-WR-CALNAME:Content
BEGIN:VEVENT
UID:<yyyymmdd>-<n>@content-calendar
DTSTAMP:<now in UTC, e.g. 20261118T090000Z>
DTSTART;VALUE=DATE:<yyyymmdd>
DTEND;VALUE=DATE:<yyyymmdd + 1 day>
SUMMARY:[<Platform>] <Topic>
DESCRIPTION:Funnel: <stage> | Format: <format>\nHook: <hook>\nBeats: <beats>\nCTA: <cta>\nMeasure: <metric>
BEGIN:VALARM
TRIGGER:-PT6H
ACTION:DISPLAY
DESCRIPTION:Post tomorrow: <topic>
END:VALARM
END:VEVENT
END:VCALENDAR
```

- In the template, `\n` means the two characters backslash and n. That is how iCalendar writes a line break inside a text field.
- In user text, escape backslash, comma and semicolon as `\\`, `\,` and `\;`, and turn real line breaks into `\n`.
- Every line ends with CRLF, including the last one.
- Fold lines so that no physical line is longer than 75 bytes, counting the leading space of a continuation line. Never split an emoji or other multi-byte character.
- In the UID, `<n>` is the post's number across the whole calendar (1, 2, 3…).
- `-PT6H` before an all-day event fires at 6pm the evening before. Apple Calendar and Outlook honour it. Google Calendar ignores reminders in imported files.

If you can write files, save both files and say where they are. If you can't, give each one in its own code block with its filename.

## Step 6: Hand-off and review loop

End with these four parts:

- **Beyond posts:** 1–3 non-content fixes for the leak, from stages-and-leaks.md. For example, a WhatsApp recall message for Not returning, or a price-enquiry reply template for Not buying. Content alone rarely closes a leak.
- **Fill in first:** list every `[placeholder]` and every "(set up first)" post, so the user knows what to supply.
- **How to import:** Google Calendar → Settings → Import & export → choose the `.ics` file and import it into a new calendar called "Content". Then set that calendar's default notification, because Google skips reminders in imported files. For Sheets or Notion, import the CSV.
- **What to track and when to review:** the 1–2 numbers from funnel-mix.md, and a review date 4 weeks from the start. Invite them back with their numbers so you can re-diagnose and plan the next period.
