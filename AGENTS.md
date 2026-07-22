> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is the API documentation site for **Mathify**, built on [Mintlify](https://mintlify.com)
- Covers the Mathify API: projects, message-driven generation, fragments, evals, and music
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- API reference is generated from `openapi.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- "Project" — a user's workspace for a generation; created via `POST /projects`
- "Message" — a prompt sent to a project that kicks off a generation; not a chat message
- "Fragment" — a single generated animation attempt, produced by a message
- "Eval" / "eval pipeline run" — automated quality scoring of a fragment (visual correctness, design, engagement rubric)

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Prefer `curl` examples with `x-api-key` for endpoint walkthroughs, matching existing pages

## Content boundaries

- Document the public API only: projects, messages, fragments, evals, music, authentication, errors
- Don't document internal render-backend implementation details or admin-only endpoints
- The legacy internal-secret auth mode is documented as legacy only — don't present it as the recommended approach for new integrations
