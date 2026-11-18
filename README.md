# Content Calendar Skill for Claude 🗓️

Most content calendars give you post ideas. This Claude skill first works out **what your business needs from content right now**, then builds a calendar that does that job and puts it in your own tools.

It's made for **SMEs, startups and personal brands**.

## What it does

1. **Diagnoses your stage:** Pre-launch, Early traction, Growth or Established.
2. **Finds your funnel leak:** are people *not seeing* you, *not trusting* you, *not buying* or *not coming back*? It works from rough numbers you already have, such as views, DMs and repeat customers.
3. **Sets your content mix:** what share of posts goes to Awareness, Consideration, Conversion and Retention. The mix depends on your stage and your leak.
4. **Gives every post a story:** a format that fits its funnel stage (myth vs truth, founder story, objection buster, customer spotlight and more), with a hook and a one-line story outline.
5. **Turns your customers' questions into posts:** the doubts people WhatsApp you before buying become your highest-converting content.
6. **Plans around real dates:** paydays, 11.11 / 12.12, Chinese New Year, Ramadan and Raya, Deepavali, school holidays.
7. **Delivers a real calendar:**
   - 📋 a dated plan with funnel stage, story format, hook, call to action and **one success metric per post**
   - 📊 `content-calendar.csv` for Google Sheets, Notion or Excel
   - 📅 `content-calendar.ics`, so every post appears in Google Calendar, Outlook or Apple Calendar
8. **Sets a 4-week review:** come back with your numbers, and it re-diagnoses and plans the next round.

> **Example diagnosis:** *You're at Early traction. Your main leak is Not buying: people DM to ask about price but few book. So this month leans on proof and objection-busting posts, not reach.*

👉 **See two real outputs:**
- [**Coffee startup (pre-launch)**](examples/coffee-startup/): its problem is not being seen, so 13 of 18 posts are for reach, followed by a waitlist launch arc.
- [**Dental clinic (established)**](examples/dental-clinic/): its problem is patients not returning, so half the posts work on bringing patients back.

`[Square brackets]` in the outputs mark facts only the business owner can fill in. The skill never invents them.

<!-- Add a demo GIF here once recorded: ![demo](assets/demo.gif) -->

## Install

**Claude Code**

```powershell
git clone https://github.com/amelialy/content-calendar-skill.git
```

Copy the whole `skills/content-calendar` folder, including `references/`, into your skills folder:

- Windows: `C:\Users\<you>\.claude\skills\`
- Mac/Linux: `~/.claude/skills/`

Then restart Claude Code and ask: *"Make me a content calendar for my business."*

**Claude.ai:** download this repo, zip the `skills/content-calendar` folder (with `references/` inside) and upload it under **Settings → Capabilities → Skills**.

## What's inside

```
skills/content-calendar/
├── SKILL.md                     # the flow: interview → diagnose → mix → plan → deliver → review
└── references/
    ├── stages-and-leaks.md      # how to diagnose stage and funnel leak
    ├── funnel-mix.md            # content mix by stage, leak adjustments, metrics
    ├── story-formats.md         # story formats for each funnel stage
    └── sea-calendar.md          # Southeast Asia festive and shopping dates
```

## Tips

- Rough numbers are fine. "Lots of views, hardly any DMs" is enough to diagnose.
- Import the `.ics` into a **new calendar** (e.g. "Content") so you can hide it or delete it in one click. In Google Calendar, set that calendar's default notification, because Google skips the reminders inside imported files.
- Be honest about how often you can post. Three posts a week, every week, beats seven posts for one week.

## Made by

[Amelia](https://github.com/amelialy), a marketer in Malaysia. If this helped, give it a ⭐.

## License

MIT
