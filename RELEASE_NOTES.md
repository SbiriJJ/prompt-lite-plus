# Prompt Lite+ 1.5

Status: public release  
Release date: 7 September 2026  
Complete executable version: 1.5.9746.29740  
Updated: 7 September 2026
Platform: 64-bit Windows  
Minimum Codex CLI: 0.152.0  
Protocol checked with Codex CLI: 0.153.4

## 1.5 changes

- New gear-button **Config** dialog for conversation/activity rolling limits,
  three conversation color presets and application update preferences.
- **Release** and **Rolling** update channels with startup/daily/weekly or
  startup/hourly/daily checks. Background downloads validate SHA-256 and the
  full fixed EXE version. Restart remains explicit and requires an idle, sole
  instance. User INI settings are preserved; package documentation is updated.
- Suggested question answers are displayed as readable, wrapped selectable
  rows. The window closes after the last reply is accepted by the server.
- **Show in Explorer** selects files through the Windows Shell API.
- Structured asynchronous agent questions are retained and displayed during
  streaming, normal history loading, and Full Load.
- **Questions (n)** opens a non-modal window with optional suggested answers
  and a free-text reply. The active task can continue while the user answers.
- Replies are sent to the original conversation, preserve the main prompt and
  its attachments, and are marked answered only after server acceptance.
- Thread metadata supplies model and reasoning during opening. Current settings
  notifications take precedence over an older resume snapshot; list refreshes
  do not change the active selectors.
- Context and limits are refreshed on model changes. Conversation token totals
  retain the server's cumulative per-thread meaning and include cached input.
- Program and document versions are aligned to 1.5. EULA acceptance follows the
  existing version/fingerprint mechanism.

Distribution: `PromptLitePlus-1.5.9746.29740-Win64.zip`.
Release packages now include the full fixed version in the filename. GitHub
provides the SHA-256 used by the updater; no manifest is required. The Rolling
channel will become available when its first build is published.

## Previous public release: 1.4

Release date: 21 August 2026  
Build: 9729  
Complete executable version: 1.4.9729.22919  
Platform: 64-bit Windows  
Minimum Codex CLI: 0.152.0  
Tested with Codex CLI: 0.152.0

## Highlights

- Fast `Ctrl+Enter` is handled without losing the shortcut or leaving a key in
  a logically pressed state.
- After a prompt is sent, the prompt editor is cleared and positioned on its
  first line.
- Incoming agent output is attached to the correct transcript block and thread
  so the first response cannot be inserted into the submitted prompt.
- The prompt editor expands into the space released when the Goal panel is not
  visible.
- Conversation backgrounds are recalculated for the new text width after a
  window resize.
- Full Load shows the speaker together with each timestamp.
- **Show in Explorer** selects the referenced local file instead of opening the
  default Explorer page.
- Multiple account-limit buckets are retained. **Limits+** identifies the
  additional data and its hint lists every available bucket.
- Pinned conversations remain in their project list and are also ordered at
  the top for quick access.
- Large thread history is loaded as summarized `thread/turns/list` pages.
  A persistent rolling-view cache is displayed immediately. Changed server
  metadata triggers a background refresh without delaying the initial view or
  downloading historical tool output and diffs into the normal conversation.
- Full Load is non-modal, uses large message-only pages, reports received pages
  and turns, can be stopped, and displays the history already received as a
  clearly marked partial transcript.
- Project conversations are selected from a compact dropdown and open as soon
  as they are selected.
- Codex CLI versions older than 0.152.0 are rejected before app-server starts.
- Codex CLI 0.152.0 app-server schemas were checked explicitly. Sub-agent,
  spawn-agent, nickname, role, parent-thread, and collaboration-state
  structures remain compatible with the current UI.

## Existing core features

- Lightweight VCL interface for Codex CLI `app-server`.
- Persistent project and conversation discovery from Codex CLI data.
- Independent multi-instance operation with one Codex CLI process per
  Prompt Lite+ instance and exclusive conversation opening.
- Runtime model, reasoning, approval, sandbox, review, and network controls.
- Tool, MCP, agent, activity, changed-file, and diff reporting.
- Bounded conversation rendering plus full transcript loading and search.
- Codex CLI detection, installation, version check, and update.
- Local staged Prompt Lite+ update support.

## Important notices

Prompt Lite+ is an independent, unofficial interface and is not affiliated with,
endorsed by, sponsored by, or supported by OpenAI.

Prompt Lite+ is hobby-developed software provided free of charge and may be
used for any lawful personal or professional purpose. It is not designed,
certified, supported, or warranted for professional, production,
safety-critical, or business-continuity use. Any such use is at the user’s
discretion and risk.

Agent operations are performed by Codex CLI under the permissions selected by
the user and remain the user's responsibility.

Prompt Lite+ depends on the Codex CLI `app-server` protocol. Protocol changes in
later Codex CLI releases may require a Prompt Lite+ update.

Read the included EULA, Legal Notice, Privacy Notice, Third-Party Notices, and
User Guide before using the application.
