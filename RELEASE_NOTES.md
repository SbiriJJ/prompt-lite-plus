# Prompt Lite+ 1.3

Release date: 5 August 2026  
Build: 9713  
Complete executable version: 1.3.9713.22639  
Platform: 64-bit Windows  
Tested with Codex CLI: 0.146.0

## Highlights

- Context usage is shown as a compact used/total bar, with an orange warning
  when usage reaches 80%.
- Account rate limits retain their original information while replacing each
  available percentage with a compact remaining-capacity bar.
- Changing the model now refreshes context and account-limit information for
  the newly selected model.
- Missing rate-limit windows remain hidden instead of displaying an empty bar.
- Idle rate-limit polling is exposed as the compact **IP** option with its
  configured interval in the hint.
- Automatic startup selection no longer interrupts a second instance when the
  conversation is already open elsewhere; the conversation area asks the user
  to select another project.
- Secondary and spawned-agent conversations are classified more reliably from
  the structured thread source supplied by Codex CLI.
- Activity, project-conversation, spawned-agent, subagent, and changed-file
  areas now provide consistent double-click guidance.
- Raize checkbox rendering is stabilized for the dark theme.

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
