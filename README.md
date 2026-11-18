# Content Calendar Skill for Claude 🗓️

Most content calendars just give you post ideas. This Claude skill first works out **what your business needs from its posts right now**, then plans posts that do that job, and puts them straight into your calendar.

It's made for **small businesses, startups and personal brands**, on any platform, with no marketing jargon.

## How it works

**1. You answer a few quick questions, mostly by clicking.**
- Where is your business right now? *(not launched yet · a few customers · selling steadily · well known)*
- What's the biggest problem? *(not many people see my posts · people see but don't message · people ask but don't buy · customers don't come back)*
- How often can you post, where, and for how long?
- Your profile link, what you sell, and what customers ask before buying

**It looks at your profile first.** It reads your public profile, without logging in, to see which posts already work for you, which don't, and whether your bio makes people want to follow. If it can't open the profile, it asks for a screenshot. Then the plan does more of what works.

**2. It tells you, in plain words, where you stand.**

> **Where you are:** You have a few customers, but not many people outside your circle know you yet.
> **What's holding you back:** People see your posts but don't message you.
> **So this month:** most posts help people trust you enough to message you.

**3. It balances your posts around that problem.** Every post has one job: **get found**, **build trust**, **get them to buy** or **bring them back**. It decides how many of each you need.

**4. It picks the right format for each platform.** A carousel on Instagram, a short video on TikTok, a text post on Threads, and so on. If you're not sure where to post, it recommends where to start. When it can search the web, it quickly checks for recent platform changes.

**5. It gives every post a story,** using everyday styles like *myth vs truth*, *founder story*, *answer a doubt* and *customer spotlight*. Each post gets a first line, a short outline and what to ask people to do. The questions your customers already ask become posts too.

**6. It plans around real dates:** paydays, 11.11 and 12.12, Chinese New Year, Ramadan and Raya, Deepavali and school holidays.

**7. You get a real calendar:**
- 📋 a dated plan in the chat
- 📊 `content-calendar.csv` for Google Sheets, Notion or Excel
- 📅 `content-calendar.ics`, so every post appears in Google Calendar, Outlook or Apple Calendar

**8. It ends with what else to fix and when to check back,** for example "send past customers a WhatsApp reminder". Come back in 4 weeks with your numbers for next month's plan.

It never makes up reviews, numbers or customer quotes. Anything only you know is marked `[fill in: …]`.

👉 **See two real outputs:**
- [**Coffee startup (not launched yet)**](examples/coffee-startup/): nobody knows it yet, so 13 of 18 posts help new people find it, ending with launch posts.
- [**Dental clinic (well known)**](examples/dental-clinic/): patients don't come back, so half the posts bring past patients back.

<!-- Add a demo GIF here once recorded: ![demo](assets/demo.gif) -->

## Install

**Claude Code**

```powershell
git clone https://github.com/amelialy/content-calendar-skill.git
```

Copy the whole `skills/content-calendar` folder, including `references/`, into your skills folder:

- Windows: `C:\Users\<you>\.claude\skills\`
- Mac/Linux: `~/.claude/skills/`

Restart Claude Code and ask: *"Make me a content calendar for my business."*

**Claude.ai:** download this repo, zip the `skills/content-calendar` folder (with `references/` inside) and upload it under **Settings → Capabilities → Skills**.

## What's inside

```
skills/content-calendar/
├── SKILL.md                  # the steps Claude follows
└── references/
    ├── profile-check.md      # how to read a profile and what to learn from it
    ├── stages-and-leaks.md   # working out where a business is and what's holding it back
    ├── funnel-mix.md         # how many posts of each kind to plan
    ├── story-formats.md      # story styles for each kind of post
    ├── platform-guide.md     # what each platform is good for, and which formats work
    └── sea-calendar.md       # Southeast Asia festive and shopping dates
```

## Tips

- Rough answers are fine. "Lots of views, hardly any messages" is enough.
- Import the `.ics` into a **new calendar** (e.g. "Content") so you can hide it or delete it in one click. In Google Calendar, turn on that calendar's default notification, because Google skips reminders in imported files.
- Be honest about how often you can post. Three posts a week, every week, beats seven posts for one week.

## Made by

[Amelia](https://github.com/amelialy), a marketer in Malaysia. If this helped, give it a ⭐.

## License

MIT
