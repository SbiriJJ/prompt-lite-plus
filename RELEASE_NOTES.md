# Prompt Lite+ 1.4

Release date: 21 August 2026  
Build: 9729  
Complete executable version: 1.4.9729.22919  
Platform: 64-bit Windows  
Tested with Codex CLI: 0.149.0

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
- Codex CLI 0.149.0 app-server schemas were checked explicitly. Sub-agent,
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
