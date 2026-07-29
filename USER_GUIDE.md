# Prompt Lite+ User Guide

Version 1.2

## 1. What Prompt Lite+ is

Prompt Lite+ is a lightweight Windows interface for Codex CLI `app-server`. It
does not provide its own AI model or OpenAI account. Codex CLI performs agent
operations and preserves compatible conversations.

Prompt Lite+ is independent from OpenAI. Read and accept the versioned disclaimer
at first startup. Use the **Disclaimer** button at the top left to read it
again.

Prompt Lite+ is hobby-developed software provided free of charge and may be
used for any lawful personal or professional purpose. It is not designed,
certified, supported, or warranted for professional, production,
safety-critical, or business-continuity use. Any such use is at the user’s
discretion and risk.

Its lightweight interface is designed for computers where the ChatGPT desktop
app causes excessive system load.

## 2. First startup

1. Start `PromptLitePlus.exe`.
2. Read the disclaimer and select **Accept and Continue**. Selecting **Exit**
   closes the application without recording acceptance.
3. Open **CLI Setup** if Codex CLI is not detected.
4. Install or update Codex CLI, or copy the displayed command and run it
   manually.
5. Authenticate using the Codex CLI login procedure when required.
6. Select a project directory and open an existing conversation or select
   **New**.

Prompt Lite+ stores the accepted EULA version and its SHA-256 fingerprint. When
the version or text of `EULA.md` changes, the disclaimer is displayed again.

## 3. Projects and conversations

Projects are grouped from the working directories reported by Codex threads.
The project name is normally the final directory name.

- Select a project to load its main conversations.
- **New** prepares a new conversation and working directory; the thread is
  created when its first prompt is sent.
- **Duplicate** forks the selected conversation into a new thread.
- **Pin** and **Unpin** preserve the selected conversation's pinned state in
  Codex CLI. Pinned conversations are marked with `[PIN]`.
- Opening a conversation reloads its current server data.
- The same conversation cannot be opened by two Prompt Lite+ instances at the
  same time.

Several Prompt Lite+ instances may run concurrently. Each instance starts its
own Codex `app-server`, allowing independent work on different conversations.

Prompt Lite+ can be used on the same computer as the ChatGPT desktop app, but
do not use both applications on the same project at the same time.

Spawn-agent conversations are available for review under their parent
conversation when the server exposes the required metadata.

## 4. Model and reasoning

Model and reasoning selections are loaded from the server catalog and belong
to the current thread. A manual change is sent to the server immediately; the
effective server notification remains authoritative.

Different threads may use different models and reasoning levels.

## 5. Permissions and safety

The settings panel exposes the protocol settings directly.

- **Approval** controls when Codex CLI asks before operations.
- **Sandbox** controls filesystem/process isolation.
- **Network access** applies where supported by the selected sandbox.
- **Auto-review** allows the configured reviewer to handle applicable
  approvals.

`dangerFullAccess` is displayed in red. It can permit operations outside the
normal workspace restrictions. Use it only when you understand and accept the
consequences.

Approvals, sandbox, and other safety settings do not make generated commands or
changes automatically correct. Review important work and maintain backups.

## 6. Sending prompts

- **Steer** is the default while a turn is active and redirects current work.
- **Append** queues or sends a normal follow-up according to the current
  server state.
- **Stop** interrupts the current turn.
- **Files** attaches file mentions to the next prompt.
- **Goal** creates, edits, pauses, resumes, or removes the persistent thread
  goal.
- **Compact** asks the server to compact the conversation context.

The Send button changes color while the agent is working. Activity status and
elapsed time are shown beside the Activity title.

## 7. Conversation and activity

The main conversation uses a configurable rolling line limit. The complete
conversation remains available through **Full Load**, with timestamps,
speaker information, and text search.

Manual scrolling disables automatic transcript scrolling. Use the down-arrow
button to return to the bottom and re-enable auto-scroll.

Activity is intentionally compact and has a configurable row limit. Tool
progress replaces the current status text instead of creating heavy animated
output.

## 8. Files, links, and diffs

Changed files are listed for the current conversation. Double-click a file to
open it. The context menu can open it, show it in Explorer, copy its path, or
display available diffs.

Transcript paths and supported URLs are clickable. Their context menu provides:

- **Open**;
- **Show in Explorer** for local paths;
- **Download** for HTTP/HTTPS links or a copy of a local file;
- **Copy link / path**.

Download remembers its own last selected directory in the local INI file and
runs without blocking the UI.

The diff form lists available file-change snapshots for the current
conversation, grouped by recent task, current Prompt Lite+ session, and date.

## 9. Token and rate information

Prompt Lite+ displays context-window use, turn/thread token totals, and the rate
information supplied by the server.

**Idle polling** requests rate information at a low frequency while no turn is
running. Token events received during work update the displayed counters
without an additional high-frequency polling loop.

## 10. Codex CLI maintenance

**CLI Setup** shows the detected executable, installed version, latest version,
and commands used for installation or update.

Only one Prompt Lite+ instance performs the startup CLI version check. A later
check may occur after the shared six-hour interval. Updating Codex CLI requires
all Prompt Lite+ instances/app-server processes to be disconnected.

CLI maintenance output is streamed into its dialog so progress remains visible.

Prompt Lite+ 1.2 was tested with Codex CLI 0.146.0.

## 11. Prompt Lite+ application updates

A local update is staged as:

```text
update\PromptLitePlus.exe
```

At startup, when Prompt Lite+ is the only running instance, it compares the
staged executable version with the running version.

If a newer version is available, the dialog displays both versions:

- **Restart and Update** closes Prompt Lite+, replaces the executable, keeps a
  `.previous.exe` backup, and starts the updated version;
- **Don't Update** continues using the current version without modifying the
  executable.

An update is never applied merely because it was detected.

## 12. Local configuration

Prompt Lite+ uses:

- the INI beside `PromptLitePlus.exe` for UI preferences, selected
  project/thread, accepted EULA version and fingerprint, rolling limits,
  conversation colors, and download directory;
- `HKEY_CURRENT_USER\Software\PromptLitePlus` for common Codex-related settings;
- shared memory only for lightweight multi-instance coordination;
- `PromptLitePlus.startup.log` for the current diagnostic session.

The first instance overwrites the startup log. Concurrent instances append to
the same log with their process IDs.

## 13. Troubleshooting

- If **Send** is disabled, connect the server first.
- If Codex CLI is missing or obsolete, open **CLI Setup**.
- If a conversation reports that it is already open, close it in the other
  Prompt Lite+ instance.
- If a project is absent, refresh after Codex thread discovery completes.
- If a thread is very large, the rolling conversation loads first; use
  **Full Load** only when the complete history is needed.
- For startup or protocol problems, copy `PromptLitePlus.startup.log` before the
  next first-instance startup overwrites it.
- For protocol incompatibility, regenerate and review the app-server schemas.

## 14. Legal and privacy

Read:

- [EULA](EULA.md)
- [Legal notice](LEGAL_NOTICE.md)
- [Privacy notice](PRIVACY.md)
- [Third-party notices](THIRD_PARTY_NOTICES.md)
