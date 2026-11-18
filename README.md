# Content Calendar Skill for Claude 🗓️

Tell Claude what you sell and where you post. In a few minutes you get a **real content calendar** that lives in your own tools, not just a list of ideas in a chat.

**You get:**

- 📋 A dated posting plan with a topic, hook and call to action for every post
- 📊 `content-calendar.csv`: open it in Google Sheets, Notion or Excel
- 📅 `content-calendar.ics`: import it and every post appears in Google Calendar, Outlook or Apple Calendar. Outlook and Apple also remind you the evening before.

It works for small businesses, freelancers and personal brands on any platform.

👉 **See a real example:** a 4-week plan for a fictional pilates studio in [`examples/`](examples/). It includes the [CSV](examples/content-calendar.csv) and the [.ics file](examples/content-calendar.ics).

<!-- Add a demo GIF here once recorded: ![demo](assets/demo.gif) -->

## How it works

1. You ask: *"Make me a content calendar for my pilates studio."*
2. Claude asks 6 quick questions: what you sell, your platforms, how often you can post, start date, upcoming events and your goal.
3. Claude plans one theme per week and rotates **Teach / Show / Prove / Ask / Offer** posts, so your feed isn't all selling.
4. You import the files and start posting.

## Install

**Claude Code**

```powershell
git clone https://github.com/amelialy/content-calendar-skill.git
```

Copy the `skills/content-calendar` folder into your skills folder:

- Windows: `C:\Users\<you>\.claude\skills\`
- Mac/Linux: `~/.claude/skills/`

Then restart Claude Code.

**Claude.ai:** download this repo, zip the `skills/content-calendar` folder and upload it under **Settings → Capabilities → Skills**.

## Tips

- Import the `.ics` into a **new calendar** (e.g. "Content"). That way you can hide it or delete it in one click.
- In Google Calendar, give that calendar a default notification so you're reminded before each post. Google skips the reminders inside imported files.
- Be honest about how often you can post. Three posts a week, every week, beats seven posts for one week.

## Made by

[Amelia](https://github.com/amelialy), a marketer in Malaysia. If this helped, give it a ⭐.

## License

MIT
