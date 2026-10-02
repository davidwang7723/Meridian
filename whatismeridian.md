# What Is Meridian

*A macOS scheduling and productivity app.*

---

## What Meridian Is

Meridian is a desktop scheduling app for macOS — built specifically for students, but useful for anyone whose week mixes recurring routines with one-off events. It lives somewhere between a calendar, a planner, a Pomodoro timer, a reminders app, a sleep tracker, and an AI assistant. Rather than asking the user to bounce between five different tools, Meridian folds all of that into one tightly integrated workspace, where the AI can read everything, edit anything, and coordinate the whole system on the user's behalf.

At its heart, Meridian is built around a simple idea: a person's week has *patterns* (the recurring stuff — class, gym, study blocks) and a person's life has *exceptions* (the one-off stuff — a doctor's appointment, a midterm, a flight). Most calendars treat these the same way and force the user to either repeat events forever or copy-paste them manually. Meridian treats them as two distinct concepts that can be layered together, edited independently, and reasoned about by an AI — which turns out to be a much more flexible way to think about a schedule.

---

## The Home Screen

Open Meridian and the first thing you see is a quiet, almost meditative home screen: a giant 72-point monospaced clock at the top, the name of whatever you're currently doing in your chosen accent color underneath it, and a soft countdown to the next thing on your schedule ("23 minutes until Gym"). If a Pomodoro session is running, its status sits inline — current task, work or break, time remaining, cycle number. A "NEXT UP" card previews the next block. Below the clock, a daily quote rotates from a library of more than 300 quotations — courage, success, wisdom, kindness, learning — seeded by the calendar date, so the same quote stays with you for the whole day and changes at midnight.

Floating around this screen are *countdown cards* — draggable little widgets the user can scatter wherever they want on the home screen. Each card tracks the days remaining until something important: "Summer Break: 15 days left," "Finals: 6 days left." They can be dragged anywhere on the screen, but the app actively avoids covering the clock or the activity name, treating those zones as forbidden regions and gently pushing cards aside if they're dropped on top. To delete one, you drag it to a trash zone in the bottom corner, which scales up and turns red as you approach.

---

## The Schedule

The Schedule tab is the largest part of Meridian, and it has two modes — Weekly and Calendar — that share data but show it through different lenses.

In **Weekly Mode**, the screen is organized around a row of day tabs (Sunday through Saturday), with today highlighted by a ring in the accent color. Selecting a day brings up its blocks, displayed as a stack of rows with start/end times in a monospaced font, the activity name, and a preview of any notes. Whichever block is currently active gets a "NOW" badge and is rendered with extra visual weight; past blocks fade to 50% opacity. Editing is fast — there's a dedicated edit button per block, but blocks can also be Shift-clicked into bulk selections and copied between days. The keyboard shortcuts feel familiar to anyone who's used a Mac: Cmd+C, Cmd+V, Delete. A floating indicator appears whenever blocks are on the clipboard, reminding you what's pending.

In **Calendar Mode**, the same data is rearranged into a traditional month grid. Each day cell shows previews of up to four blocks — activity names in their assigned color, start times — with a "+X more" badge if the day is overbooked. A resizable sidebar shows the selected date, the count of blocks on it, and shortcut buttons for copying and pasting days. There's also a "Today" button to jump back to the present, and a "Plan Your Week" flow for batch operations.

That "Plan Your Week" wizard is one of Meridian's most useful features. Instead of forcing the user to add events one at a time, it opens a three-stage process: first, edit a representative week of blocks in a compact mini-editor; second, pick which upcoming weeks (grouped by month, with checkbox selection per month) should receive that week's pattern; third, confirm. Behind the scenes, Meridian then *projects* that week's blocks across the chosen weeks as actual calendar blocks. It's the difference between writing a recurring event rule and authoring a finite, editable schedule the user can adjust week by week. The wizard pairs naturally with a *templates* system — the user can save the current week as a named template ("Summer Schedule," "Exam Prep"), then reuse it later in a click.

When the user edits a recurring block from within Calendar Mode, the app asks an important question: *which occurrences?* It offers three options — this single occurrence (which silently converts the recurring entry into a one-time override), this whole week's occurrences (which generates a skip-marker), or all occurrences (which edits the underlying template). It's a small decision but it's the kind of detail that separates a tool that works *with* you from a tool that requires constant cleanup.

There's also a custom color palette of **32 colors** — not Apple's defaults, but a carefully chosen set including Lavender, Sage, Rust, Crimson, Turquoise, Mint, Salmon — so users can color-code activities meaningfully (all "Gym" blocks purple, all "Study" blocks blue) without their schedule looking like every other app's calendar.

---

## Pomodoro

The Pomodoro timer is a small, self-contained productivity loop inside the larger app. Setup is direct: name the task ("What are you working on?"), set work and break durations (defaulting to 25 and 5 minutes), choose the number of cycles (defaulting to 4). The app shows clear error states if the task name is blank or the durations are zero. Saved configurations can be stored as *presets* — a horizontally scrolling row of named templates ("Deep Work: 25m / 5m × 4," "Sprint: 50m / 10m × 3"). Tapping a preset starts that session immediately.

Once started, the timer takes over with a circular progress ring (accent color for work, green for break) that shrinks as time counts down. The center shows the mode (WORK or BREAK), the task name, and a giant monospaced countdown. Cycle progress is displayed beneath it ("Cycle 3 of 4"). The session can be paused, resumed, or ended at any time.

Where Meridian's Pomodoro shines is in the notifications. They're not generic — they're written with personality:

- **At start:** "Start doing [task] now! Cycle 1/4 — Stay focused 💪"
- **At break:** "Take a break! Cycle 1/4 done — Relax for 5 minutes 😌"
- **5 minutes before the final work session ends:** "5 minutes left — wrap it up! ⏰"
- **At the end of the final work session:** "Work done — pack up! 🎒"
- **When all cycles are complete:** "All done! Congrats! 🎉🥳"

The state of the Pomodoro is persisted continuously to disk, so if the user quits the app or restarts the Mac, the timer picks up right where it left off. It means the user can trust the timer, which means they're more likely to actually use it.

---

## Reminders, Assignments, and Countdowns

The Reminders and Assignments tab handles two related but distinct kinds of work: things that need to happen at a particular time (Reminders) and things that are due by a particular time (Assignments).

**Reminders** are sortable by date and support four recurrence patterns: one-time, daily, weekly, monthly. Each reminder has a checkbox that completes it (a one-second delay before deletion gives the user a chance to undo), a recurrence badge, and an "OVERDUE" tag with day count if it's past due. Recurring reminders auto-reschedule themselves once fired — the user never has to manually re-create them.

**Assignments** (homework) are a sibling concept: a title, an optional subject tag, a due date, and a configurable notification time (default 18:00 the day before). The list shows only unfinished assignments, sorted by due date, with badges for OVERDUE or TODAY. Each row has a "Do this" button that primes the Pomodoro timer with the assignment as the task — a small but useful bridge between planning and doing.

**Countdowns** are the third member of this family — but instead of triggering notifications, they live visually on the home screen as draggable cards. They're for the long-horizon things: trips, holidays, exams, deadlines. Their job is to be quietly visible.

---

## Theming, Typography, and the Onyx Mode

Meridian has two visual themes: **Bright** and **Onyx**.

Bright is a near-white interface (#F5F7FB background, white surfaces) with soft contrast and a clean, paperlike feel. Onyx is a deep dark mode (#0D0D12 background, #1A1A21 surfaces) tuned for low-light use and high text contrast. Users can lock the app to either theme, or switch on **Dynamic Mode**, which automatically transitions between them on a schedule the user defines (default: Onyx at 7 PM, Bright at 6 AM). The transition isn't a hard cut — it's a smooth 0.4-second ease-in-out animation, so the change feels intentional rather than abrupt.

Layered on top of the themes is an **accent color** system: eight built-in colors (Blue, Sky, Green, Orange, Red, Purple, Pink, Teal), with the option to set any hex value via the AI chat. The accent color tints the activity name on the home screen, the active block ring, the Pomodoro work ring, and most other interactive elements.

The typography is carefully tuned. The clock is 72-point ultralight monospaced. Activity names are 38-point semibold. Block times are 12-point medium monospaced. There's a **font scale slider** in Settings that ranges from 0.7× to 1.6× and applies globally to every text element in the app, accessible for users with vision needs or simply users who want the clock visible from across the room.

---

## The Menu Bar

Meridian sits in the macOS menu bar as a status item. By default it shows a single inline string summarizing the current state of the app:

> Current session: Study · 🍅 Pomodoro: work (22:05 left) · ⏰ Reminder: Call mom: 2h left

It updates every second. The user can collapse it into a compact ⏰ icon if they want their menu bar to stay clean — on hover, a custom popover slides down with all the same information laid out vertically. The hover detection polls the mouse position at a short interval to keep CPU use low while preserving a snappy feel, and the popover stays visible as long as the cursor is in either the icon or the popover itself, even while traversing the gap between them.

Right-clicking (or click-and-hold) the menu bar item opens a quick menu: Add Schedule Block, Add Reminder, Add Assignment, and — if Pomodoro is running — Pause, Resume, or End. These are the most common actions, made accessible without ever opening the main app window.

---

## The AI Chat

This is where Meridian becomes more than a scheduler. Pressing **Cmd+J** (or whichever letter the user has chosen) opens an AI chat panel — either as a sidebar inside the main window or as a floating, blurred-glass companion window. The AI sees the user's entire schedule context: the current time, day, and timezone; every recurring block; the past 30 days and all future calendar blocks; active countdowns, reminders, and pomodoro state; even the user's display preferences and unread email.

What makes it powerful is what the AI is allowed to *do*. Meridian wires up structured action calling: the assistant can respond with fenced ` ```action ``` ` blocks containing JSON, and the app interprets them as commands. The actions include:

- `add_block`, `edit_block`, `delete_block` — manage weekly recurring blocks
- `add_calendar_block`, `delete_calendar_block` — manage one-off events
- `add_weekly_to_calendar` — project a weekly pattern across a date range
- `add_countdown`, `delete_countdown` — manage countdown cards
- `add_reminder`, `delete_reminder` — manage reminders
- `start_pomodoro`, `pause_pomodoro`, `resume_pomodoro`, `end_pomodoro` — control the timer
- `add_pomodoro_note` — append a timestamped note to the Pomodoro notes panel
- `set_display_mode`, `set_accent_color`, `set_font_scale`, `set_timezone` — adjust app settings
- `send_email` — draft and, on confirmation, send a Gmail reply

So the user can simply say *"plan my Monday with gym, work, and study"* and the AI will respond with three add_block actions, each of which appears in the chat as a pending confirmation card. Destructive actions (delete, edit, send email) require explicit approval via an orange "✅ Confirm" button. If more than three confirmations are pending, an "Approve All" button appears for bulk approval. This gives the user a chance to inspect every action before it takes effect — the AI suggests, but the user remains in control.

Meridian supports nine AI providers — Gemini (default), OpenAI, Anthropic, DeepSeek, Grok, Mistral, Groq, Doubao, and **Ollama** for fully local models — with model selection per provider. API keys are stored locally and managed per-provider via a dedicated key entry sheet with documentation links. Because the same provider and key drive the chat, the Pomodoro notes, and the email-reply drafts, choosing a provider once applies everywhere — including a local Ollama model, which keeps every AI request on your own machine.

---

## Calendar and Email Integration

Meridian can import events from both **Apple Calendar** (via EventKit) and **Google Calendar** (via OAuth 2.0). Both flow through a unified three-stage import wizard: pick which events to import, edit them in a preview, and choose which weeks they should be projected onto. Apple Calendar access is read-only and respects the system's calendar permissions. Google Calendar uses a Cloudflare Worker as a token-exchange proxy so the OAuth client secret never ships inside the app; it listens on localhost:8080 for the OAuth redirect and handles refresh-token renewal automatically.

Imported events become *calendar blocks* — the same one-off block type the user creates manually — so they get treated identically in the rest of the app: they show up on the home screen, in the schedule, in the AI's context, and in the menu bar.

Meridian also connects to **Gmail**. It can read your unread inbox, surface those messages to the AI as context, and draft replies in natural language — which you review and send with a single confirmation. Nothing is sent without your explicit approval.

---

## Sleep, Wake, and the Quiet Background Logic

Meridian includes a built-in sleep schedule. The user sets a bedtime and a wake time, and the app does two things: it automatically inserts a "Sleep" block onto every day's schedule (so the schedule reflects reality), and it sends two pre-bed notifications — one 10 minutes before bedtime ("Sleep in 10 mins 🌙") and one at bedtime itself.

Quietly under the hood, the app does a lot of background work. Notifications are de-duplicated so the same alert doesn't fire twice. Each notification category (Pomodoro, Sleep, Schedule, Reminder, Homework) can independently be set to *notification* style (a normal banner) or *alarm* style (a looping system sound with a modal window the user has to dismiss). Recurring reminders re-schedule themselves automatically. Yesterday's countdowns auto-expire. The Pomodoro state persists across restarts. Global hotkeys are re-registered if the user changes them. The menu bar updates every second. The dynamic theme switches at the configured times.

None of this is exposed as a setting the user has to manage — it just happens. That's the design philosophy of the app: surface what the user needs to see, hide what they don't.

---

## Home-Screen Widgets

Meridian ships a WidgetKit extension, so parts of the app live on the macOS desktop and in Notification Center without opening the main window. There are three widgets: the **current session** (what you're doing now and what's next), a **Pomodoro ring** that drains as the active segment counts down, and a **reminders** list. They read a shared snapshot the app writes on change, so they stay current while sipping almost no energy.

---

## Under the Hood

Meridian is a single Swift file — mostly SwiftUI, with strategic AppKit where SwiftUI falls short (the menu bar, the floating chat window, the OAuth localhost server, the global hotkey integration), plus the WidgetKit extension. It uses no third-party dependencies. Data is persisted as JSON files in Application Support — one file per entity type (schedule, calendar blocks, reminders, homework, countdowns, semesters, week templates, pomodoro presets, settings), all written atomically. There's no database, no migration layer, no ORM — just structured Codable types and a small storage manager.

For performance, the app maintains an in-memory index that maps date strings to lists of calendar blocks, so date lookups are fast instead of scanning the full block list every time. Drag operations use SwiftUI's `GestureState` so they don't trigger full view re-renders. Timer-based updates run at 1-second granularity instead of continuous reactivity. These choices keep the app responsive even with thousands of blocks.

The app integrates deeply with macOS frameworks: **SwiftUI** for the interface, **AppKit** for the menu bar and floating windows, **WidgetKit** for the desktop widgets, **EventKit** for Apple Calendar, **UserNotifications** for alerts and alarms, **Carbon** for global hotkeys, **URLSession** for AI-provider and Google HTTP calls, and raw **BSD sockets** for the Google OAuth localhost callback.

---

## What Meridian Is Really About

Step back from the feature list and a picture emerges. Meridian is, at its core, a *control surface* for a student's week. A good control surface needs more than buttons: it needs to feel quiet when there's nothing happening, alive when something is, and forgiving when the user makes a mistake. It needs to know the difference between routine and exception. It needs to make the common things easy and the destructive things deliberate. It needs to remember what the user told it.

The features that stand out aren't the obvious ones — they're the small ones. The way a countdown card refuses to sit on top of the clock. The way the Pomodoro timer survives a Mac restart. The way the AI's destructive actions queue up for confirmation instead of just running. The way the daily quote is seeded by the date so it doesn't change while you're reading it. The way the dynamic theme transition takes 0.4 seconds instead of switching instantly. The way the "Plan Your Week" wizard projects a single week onto twelve future weeks at once. The way the menu bar text updates every second and collapses to a single icon when you want it out of the way.

Meridian isn't trying to be everything to everyone. It's trying to be one student's complete operating system for their week — a place where time, plans, focus, reminders, and email all live together, where an AI can help shape that week without taking it over, and where the visual experience stays calm enough to live with all day long.
