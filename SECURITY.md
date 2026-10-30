# Security

These plugins run inside Codex on the user's own machine. Session Stats reads the local Codex session index and session logs, which can hold private conversations, file contents and credentials that passed through a session. It is meant to read them without changing them, keep their text out of everything it writes, make no network requests, and write only into the output directory it is given.

## Reporting a vulnerability

Please do not open a public issue for a security problem. Report it privately through GitHub: **Security → Report a vulnerability** on this repository ([direct link](https://github.com/nervouna/codex-plugins/security/advisories/new)). Include what you did, what happened, the plugin version and the Codex version. Do not attach real session logs; a minimal made-up example is enough.

You will get an answer within a week. Fixes land on `main`; there are no maintained release branches.

## In scope

- A way to make a plugin write session text, tool arguments, tool output or other private data into a snapshot, its receipt or its error messages
- A way to make a plugin modify or delete Codex data, or write outside the output directory it was given
- A way for a session reference or session content to make a plugin run code or send data over the network

## Out of scope

- Anything that needs prior write access to the user's Codex home or home directory
- Problems in Codex itself, or in how the Codex App displays a snapshot
