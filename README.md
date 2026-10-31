# Mandible for AI assistants

Mandible is the dentist's cockpit: an everything app for dentistry. This repo connects your Mandible records to
Claude Code and Gemini CLI. The server is Mandible's hosted MCP server at `https://api.mandible.io/mcp/listed`: read-only, your own records only, OAuth
sign-in with a Mandible account. No code from this repo runs on your machine.

## Claude Code

```
claude plugin marketplace add WeirdBrains/mandible-ai
claude plugin install mandible@mandible
```

Then run `/mcp`, pick `mandible` and choose Authenticate.

## Gemini CLI and Antigravity CLI

```
gemini extensions install https://github.com/WeirdBrains/mandible-ai
```

Then run `/mcp auth mandible`. The repo carries the `gemini-cli-extension` topic so the Gemini extensions gallery lists it.

## Claude.ai, Claude Desktop and ChatGPT

Add a custom connector with the URL `https://api.mandible.io/mcp/listed`, then sign in to Mandible.

## Example prompts

- What do I still need before my license renewal?
- What expires in the next 90 days?
- How many CE hours do I have this year, by category?
- Which study clubs am I in, and what events are coming up?

## What it can read

Your profile, licenses and credentials (numbers masked to the last four digits), CE hours by category, renewal
readiness against your state board's rules, memberships, the spaces you belong to and their events. It does not
read patient records, clinical cases or images, and it never writes or submits anything.

Disconnect at any time in Mandible under Settings > Connected apps.

Privacy: https://mandible.io/privacy-policy. Terms: https://mandible.io/terms-of-service. Support:
https://mandible.io/support.
