# Meridian

A schedule, an assistant and a clock for the Mac, in one app.

Meridian replaces the five apps most people run their days from: a calendar, a to-do list, reminders, a focus timer and a chatbot in a browser tab. Its assistant, Sol, sees all of it and can change any of it when you ask, typed or out loud, and nothing changes until you say yes.

Free. Website: [meridian-63u.pages.dev](https://meridian-63u.pages.dev). Every version's changes: [CHANGELOG.md](CHANGELOG.md). A longer tour: [whatismeridian.md](whatismeridian.md).

This repository holds releases and documentation only. The source code is not public.

## Download

Get the latest DMG from [Releases](../../releases/latest). Each release lists its VirusTotal scan and SHA-256, and the website's [Scan it yourself](https://meridian-63u.pages.dev/scan-yourself.html) page shows how to check the file before you open it.

## Install

1. Open the DMG and drag Meridian onto the Applications folder.
2. The first time you open it, macOS says it cannot check the developer. Meridian is signed but not notarised by Apple, so this is expected. Click Done, open System Settings, Privacy & Security, scroll down and click **Open Anyway** next to Meridian.
3. If that button does not appear, run this in Terminal, then open Meridian again:

   ```
   xattr -dr com.apple.quarantine /Applications/Meridian.app
   ```

After that, Meridian updates itself from Settings.

## Requirements

- macOS 15 Sequoia or newer. Liquid Glass needs macOS 26.
- Apple Silicon (M1 or later). Releases before v1.20.0 also run on Intel Macs.
- Sol needs an AI model: a key for a cloud provider, a coding agent you are signed in to, or a model running on your own Mac through Ollama.

## What it does, and how far each part goes

### Home

A large clock in the middle of the window in the face you choose, with what is on now, what comes next and a countdown to it.

- Second clocks for other cities, with how far ahead or behind they are.
- The weather now, the day's high and low, and the date. Click to switch between Celsius and Fahrenheit.
- Countdown cards you place anywhere on the page.
- Unread mail from Gmail or the Mac's Mail app.
- Holidays named on the day, for the regions you choose, checked against published calendars through 2030. A few occasions bring their own animation; nothing generic.

### The schedule

Three views of the same days: a month **Calendar**, a **Weekly** timeline and a **Daily** list.

- Click an empty slot for an hour, or drag to draw a session of any length, across several days at once.
- Drag to move, drag an edge to resize, Esc to let go mid drag.
- Overlapping sessions are drawn one inside the other (a review inside Study Hall), and a session can run past midnight into the next day.
- Every session is one-off or repeating. Editing a repeating one asks which ones you mean: this one, this week's or every one.
- **Templates** for a day or a week, laid over any future days as real, editable sessions.
- **Rotations** for schedules that do not follow the weekdays: A to G school days, four on three off shifts, training cycles. Skip days, push or pull the whole rotation a day, and each day is named with its letter.
- Thirty two session colours chosen to tell apart at a glance.

### Tasks, assessments and the checklist

- A **task** has a due date and real work behind it. Meridian estimates the work (or takes yours), finds free time before the due date and proposes sessions on a timeline for you to confirm. Fall behind and it plans the rest again. A small task, under the length you set, just gets reminders before it is due.
- An **assessment** (a test, an exam, a quiz) has a date and units. Sol estimates the review time, says whether to spread it out or cram, and plans review sessions that stay tied to it: move, split or add one and the total time is kept. Any session can be linked to an upcoming assessment.
- **Review time counted as it really went.** Each review session counts as you kept it, moved, cut short or stretched, and as you answered about it; one that happened stays counted after you delete it.
- **The checklist** is one list of lines to tick, on the right of the menu bar card and in a Checklist window on Home. Unticked items carry over to the next day. Put an item under a class and it sits with that class's other items, in a frame of the class's colour.
- An **Up next** card says which step of which task is next and how far through it you are.
- Give a task or assessment the link to its assignment, rubric or unit page and Sol reads it and keeps notes.
- **How was the time?** After a session, a focus run or a review, Meridian asks whether the time was right and learns from your answers, so the next estimate is closer.

### Reminders and medicine

- Once or on repeat: daily, chosen weekdays, every second or third week. Each keeps the time zone it was made in, so a reminder for 8 at home still means 8 at home when you travel.
- **Medicine** is its own kind: a course with doses per day, times, an end date, and a check for whether each dose was taken. It always rings.

### Notifications and alarms

- Each kind (schedule, reminders, tasks, sleep, focus) is a **banner** or an **alarm**, chosen per kind.
- Banners are Meridian's own, so Focus modes do not hide them, and can carry buttons such as snooze and done.
- Alarms float above every window on every desktop until you answer, ringing a system ringtone or your own sound.
- Volume per kind and per output (headphones, Mac speakers), from 5% to 800%: the Mac's volume is raised first and the rest is amplified. Meridian never lowers your volume and puts back what it raised.
- **Interrupt** pauses whatever is playing before an alarm rings and resumes it after.
- **With the lid shut**, a small helper wakes the Mac for alarms and keeps it awake while they ring.
- Bedtime and wake time, and a different wake time for tomorrow only.

### Focus

A Pomodoro timer with presets, a notes pane for the session (formatting and timestamps), and a timer that survives quitting the app or restarting the Mac.

### Sol, the assistant

- **Sees everything in the app**: schedule, tasks, assessments, the checklist, reminders, rotations, countdowns, settings and your earlier chats. Ask "am I free Thursday afternoon?" and it looks, rather than guessing.
- **Changes anything** you ask in your own words: "move dinner to 7", "plan my essay", "I finished the report", "wake me at 6:15 tomorrow".
- **Nothing without your OK.** Every change is a card, and the card plays the change on a small timeline before you confirm. A permissions switch lets changes go through without cards, except email and anything risky on your Mac. Sol's own planning windows always ask.
- **Meridian reads first.** Plain questions ("what's next", "time in Tokyo") are answered instantly and offline, and plain changes become a card directly, before any model is asked.
- **Checks its own work.** Sol tries each change before you see it, fixes what fails, and is held to everything you said ("except study hall" is kept).
- **Planning windows.** Planning an assessment or task opens a window just for it: the conversation beside the proposed sessions on a timeline, then Done planning.
- **Plans that run on their own.** Settings, AI, Plans: steps for Sol, a time and the days. Sol runs them, catches up when the Mac was off, and brings anything it wants to change to you in a window of its own. A plan marketplace lets you get plans other people made and share your own.
- **The web**: search and read pages, naming its sources.
- **Your Mac**: Sol can work in apps, a browser and the terminal, step by step, with a plan shown above the chat. It asks before anything dangerous (deleting files, system or security settings).
- **Music and video**: pause, play and skip in Spotify, Music, Chrome or other apps.
- **MCP servers**: connect your school's LMS or any MCP server by pasting a link, command or config from Claude, Cursor or VS Code. Read-only tools run without a card.
- **Pictures and PDFs**: drop them on the chat, and models that can see get the picture itself.
- **In the chat**: charts, flashcards and quizzes, Reply to part of an answer, and Read aloud in Sol's voice.
- **Themes** in any colours or mood you describe, and edits to the ones you have.
- **Contacts**: add people from Contacts so Sol can call them.
- **Your choice of model**: Gemini, Claude, OpenAI, DeepSeek, Grok, Mistral, Groq or Doubao with your own key; Claude Code, Codex or Gemini CLI signed in with your own account; or a model on your own Mac through Ollama, where nothing leaves the machine.

### Voice mode

- "Hey Sol" opens it hands-free; it learns your voice from a few recordings.
- Sol answers out loud sentence by sentence while it is still writing, so it starts almost at once.
- Cut in any time: your voice at the Mac pauses Sol, the room's talk does not. Echo cancellation keeps Sol from hearing itself.
- Neural voices that run on the Mac (Pocket TTS, Supertonic, MeloTTS), each with its own volume, and listening in many languages, including Chinese shown live as you speak.
- Say goodbye, in any words, and the window closes.

### Morning and night check-ins

- **Morning**: Sol reads you your day the moment you stop the wake-up alarm, or offers it the first time you unlock the Mac: the weather, your first session, what is due, work planned for tasks, reminders, a summary of your email and the headlines. It pauses your music first and resumes after, with a card to read along, pause, or act on ("Plan Biology with Sol"). Ask Sol to add something to tomorrow's.
- **Night**: go over what is left, move it all to tomorrow in one press, and set what to be reminded of in the morning.

### Wallpaper, screen saver, menu bar and widgets

- **Wallpaper**: the clock, Next up and the weather drawn on your desktop, over your own picture, one of Meridian's or your Mac's wallpaper. Countdowns can be dragged anywhere; hold Command over the weather or Next up to drag them.
- **Screen saver**: the same clock over your current desktop's wallpaper.
- **Menu bar**: what is on now and next, a new session, and quick access to everything.
- **Widgets** for the desktop and Notification Center in your theme's colours: current session, tasks and reminders, and the focus timer.

### Looks

- Display modes Bright, Onyx, Dynamic (switched at times you set) and System, plus accent colours.
- **Themes**: built-in ones, ones you make with a live preview, and ones Sol designs. A light theme by day and a dark one at night, switched automatically. Every theme but Bright and Onyx can be edited or deleted.
- Fonts for the clock and the app, a text size, and Liquid Glass over a photograph.

### Languages

Thirty two languages: seven built in (English, Simplified Chinese, Hindi, Spanish, Arabic, French, Bengali) and twenty five more that download when picked. Sol answers in the app's language, and voice mode listens and speaks in every language that has a voice.

### Privacy and upkeep

- Your schedule, notes and chats are files in your own Library. Nothing leaves your Mac except what goes to the AI provider you pick, and with Ollama not even that.
- Keys and sign-ins are kept in the macOS Keychain.
- Built to sit open all day at the energy cost of an idle app.
- Updates download and install from Settings, with notes on what changed.
- A suggestion box in Settings sends ideas straight to the developer.

### Credits

The Earth behind the clock on Earth Day is drawn from NASA's Blue Marble imagery (NASA Visible Earth).
