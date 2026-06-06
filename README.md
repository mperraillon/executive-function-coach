# Coaching System — Setup Guide

A personal executive function coaching system built on plain markdown files and Claude. Designed for students and early-career researchers who need more structure, more follow-through, and a sense of urgency on long-horizon work that has no immediate deadline. The guiding principles are based on my experience and the insights from the book Inside the Box by David Epstein. The book describes the usefulness of internal and external constraints on creativity and other outcomes. The more the coaching sysmte is used, the better it works since it creates "memories" based on patterns detected. Memories are just a collection of text files (markdown) with lessons learned through the use of the system. 

## What this is

A folder with a few markdown files Claude (or another similar system) reads and writes to as you work with it. There is no app to install, no subscription, nothing that can break. The data is plain text, readable by any editor, syncable through Dropbox or iCloud.

Claude reads the protocol from `CLAUDE.md` at the root of this folder and acts as your coach/assistant. You talk to it in plain language ("morning," "check in," "shutdown," "weekly review"). It runs short protocols, writes structured logs, and over weeks builds a longitudinal record that no human coach could hold in memory.

The coaching style is warm, direct, and willing to push back. It is not a cheerleader. It will tell you when a task is drifting, when a deadline you set with yourself counts as real, and when you are confusing "I worked hard" with "I shipped the thing."

## What you need

1. **Claude Code** installed on your laptop. Free download: claude.com/claude-code. This is the terminal interface that lets Claude read and write to your files. (Claude on the web or in the app cannot do this — file access is the point.)
2. **A sync service (not needed if you always work in the same computer)** (Dropbox, iCloud, Google Drive). Put this whole folder inside it so you can use the system from any device that has Claude Code.
3. **An editor** for browsing your logs. VS Code is good. Obsidian is excellent if you want to see the parking lot and patterns visually.

## Extensions

Because I work from multiple devices, I set up NanoClaw so an "agent" has acess to the folder and I can communicate with the coaching system via Slack. NanoClaw has many more communication channels.  

## First-time setup

1. Place this folder somewhere inside your sync service (e.g., `~/Dropbox/Coaching/`).
2. Open `CLAUDE.md` and replace every `{{NAME}}` placeholder with your own first name. Save.
3. Optionally fill in the `## About me` section near the top of `CLAUDE.md` — what you're working on this semester, what's hard, what you tend to defer. The coach will use this. Honest beats polished.
4. Open the folder in Claude Code: `cd ~/Dropbox/Coaching && claude` (or open the directory through the Claude Code app).
5. Type: **"morning triage"** — your first session begins.

## Daily rhythm

| When | What you type | What happens |
|---|---|---|
| Morning (~15 min, live) | "morning," "triage," "start my day" | Coach reads yesterday + patterns, asks what's on your mind, helps you pick **3 tasks max**, specifies the first physical action for each. Writes today's log. |
| Midday (~5 min, optional) | "check in," "I'm stuck" | Coach asks what you've touched, helps decompose blockers, captures off-list pulls. |
| Evening (~10 min) | "shutdown," "done for today" | Coach walks completions, asks about restorative time, captures carries, writes the day summary. |
| Anytime curiosity strikes | "parking lot time," "I want to explore" | Coach opens the parking lot, sets a soft time-box, logs what you found. |
| Sunday evening (~45 min) | "weekly review" | Coach reads all 7 daily logs, surfaces drift patterns, sweeps the to-do list, asks calibration questions. Triggers automatically on Sunday shutdown. |

You do not need to do every protocol every day. The system is designed to recover from gaps — miss a morning, do shutdown. Miss a shutdown, do triage tomorrow. Skipping is not failure.

## What accumulates

After two weeks you have a longitudinal record of what you actually did versus what you said you would do. After eight weeks you have evidence of which days collapse and what precedes them, which interests are real and which are dopamine spikes, and which "soft deadlines" never produce work. The coach uses this to push back on you specifically, not generically.

This accumulation is the entire point. A single day's plan is useful; eight weeks of plans reviewed by an AI that never forgets a carried-forward task is transformative.

## Tuning for urgency

This bootstrap is tuned for someone who needs **more external pull on long-horizon work**. The morning triage explicitly asks who is expecting each item; the weekly review surfaces anything due in the next 14 days that hasn't entered a daily log yet; the coach will push back if you list a "soft" task with no one waiting on it. Read `CLAUDE.md` and adjust if your situation is different (e.g., if you have *too much* external urgency and need help saying no instead — the tuning would invert).

## Files in this folder

- `CLAUDE.md` — the coaching protocol. The system prompt Claude reads.
- `templates/daily.md` — template for daily logs (Claude fills it in for you).
- `templates/weekly.md` — template for weekly reviews.
- `parking-lot.md` — your second brain for ideas you want to explore but not now.
- `patterns.md` — Claude's running hypotheses about how you work.
- `to-dos.md` — your master list of things you want to do at some point. Quiet; read during weekly reviews.
- `constraints-working-reference.txt` — distilled principles from David Epstein's *Inside the Box*. The coach uses these as a lens.
- `logs/daily/` and `logs/weekly/` — auto-created on first use.

## Principles for sustainability

- **Missing a day is not system failure.** The system recovers; you do not need to apologize to it.
- **Three is a ceiling, not a quota.** Two tasks is fine when the day is constrained. Don't pad.
- **The parking lot is sacred.** Never let it become a second to-do list. Nothing in it is obligatory.
- **Tune everything.** The weekly review exists to modify any parameter. If three tasks is too many, drop to two for a few weeks. If the morning session is too long, shorten it. The structure serves you, not the other way around.

Open Claude Code in this folder and say "morning."
