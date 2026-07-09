# Documentation project instructions

## About this project

- This is the documentation site for the **Cloak Bot SDK** (`@cloak/bot-sdk`), the official TypeScript SDK for building end-to-end encrypted bots on [Cloak](https://cloak.chat).
- Built on [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.
- The SDK source lives in a separate repo. When documenting an option, method, event, or type, verify it against the real SDK surface before writing. Do not invent API.

## Audience and scope

- Write for a **developer building a bot**. Assume they can write TypeScript and may have built a Discord bot before.
- Document only what a bot author needs. Do **not** document SDK internals: transport and QUIC framing, crypto wire formats, libsignal revision pinning, the `src/` file layout, the test suite, or contributor workflows.
- The encryption model is in scope at a conceptual level, because it shapes how bots behave (keystore, first-join key handoff, view-gated delivery).

## Terminology

- "server" and "guild" both appear. Prefer "server" in prose; note that the SDK types call it `Guild` (discord.js naming) where relevant.
- "bot token", not "API key".
- "keystore", not "key file" or "key store".
- "firehose" for the delivery model. "grant" for resolved permissions, "declare" for requested ones.

## Style preferences

- **No em dashes.** Use commas, colons, parentheses, or separate sentences instead. This is a hard rule.
- Avoid AI writing tropes, including "it's not just X, it's Y" and "X isn't Y. It's Z." constructions.
- Use active voice and second person ("you").
- One idea per sentence. Keep sentences short.
- Sentence case for headings.
- Bold for UI elements: **Settings > My Bots**.
- Code formatting for names, commands, paths, and code references.
- Every concept and reference page ends with a "Next" section of `<Card>` links.

## Brand

- Primary color is Cloak Blue `#57aaf2`. In `docs.json`, `primary` is `#2e76e2` (legible on light backgrounds), `light` is `#57aaf2` (dark mode), `dark` is `#234585`.
- Font is Source Sans 3.
- Logos and favicon are sourced from the Cloak app assets. Light-mode logo uses a dark-ink wordmark with the blue icon; dark-mode logo uses a white wordmark with the blue icon.
