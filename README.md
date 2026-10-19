# Yadulink for Claude

Manage LinkedIn outreach from a conversation with Claude. Yadulink brings your
contact priorities, inbox, lists, sequences, and growth analytics into the same
workflow, while keeping actions within the permissions of your Yadulink account.

## Five workflows

- **Morning priorities:** decide who to contact today and understand why.
- **Inbox triage:** summarize conversations, identify follow-ups, and draft replies.
- **Find prospects:** preview a targeted search and its credit cost before importing a list.
- **Sequence next step:** audit an outreach sequence, prepare changes, and request separate approval before launching it.
- **Weekly growth:** review progress, pipeline leaks, and opportunities for the next week.

Try: “Who should I contact today and why?”, “Summarize my LinkedIn inbox and draft
three replies without sending them”, or “Audit my active outreach sequence and
suggest the next improvement.”

## Connect your account

1. Install this plugin in Claude.
2. Open the plugin's **Connectors** tab and connect **Yadulink**.
3. Sign in to Yadulink and review the OAuth permissions before authorizing Claude.
4. Ask for one of the workflows above.

You need a Yadulink account with active product access. Searches and LinkedIn
actions require a connected LinkedIn account, available credits where applicable,
and the corresponding account permissions. The available tools depend on the
OAuth permissions you authorize. Workspace access is checked by Yadulink.

For Claude Code, the plugin uses the same remote HTTP MCP server. Complete its
OAuth connection from the MCP connection controls. No API key is bundled or
required in the plugin files.

## Actions and limits

An analysis request does not authorize importing contacts, sending a message, or
launching outreach. The workflows show the audience, content, timing, and quoted
cost before asking for approval of a write. Creating a prepared sequence and
launching it are separate approvals. Account limits, idempotency checks, and
server-side authorization continue to apply. Draft replies are not sent.

## What the plugin runs and sends

This package contains five Markdown skills and one remote MCP configuration.
It has no local executable, installation script, hook, or background process.
The declared MCP destination is **https://mcp.yadulink.com/mcp/**. Authentication
uses Yadulink's OAuth service on **https://app.yadulink.com**.

When you request a workflow, Claude sends the relevant tool arguments to Yadulink.
Yadulink returns the account-scoped records needed for that request, which can
include profile details, contacts, message content, lists, sequence configuration,
and analytics. The plugin does not request Claude's unrelated chat history,
memory, or files. Yadulink logs tool execution metadata for security, diagnostics,
support, and auditing. LinkedIn operations use Yadulink's backend integration via
Unipile for the account you have connected; they are not direct calls from these
plugin files. Applicable Yadulink subprocessors are listed in the privacy policy.

The plugin itself maintains no additional datastore. Data processed by the
Yadulink service is retained as needed to provide the service and until account
deletion, subject to legal retention requirements. OAuth authorizations remain
while the connection is active; technical logs follow the security and support
retention described in the privacy policy. Disconnect the connector to revoke
its access, and contact support for account data requests.

## Help and policies

- [Product and account access](https://yadulink.com)
- [Documentation](https://docs.yadulink.com/)
- [Privacy policy](https://yadulink.com/privacy-policy)
- [Service terms](https://yadulink.com/cgv)
- Support: **support@yadulink.com**

Published by **AVICLICK (YADULINK)**. Yadulink is independent of LinkedIn and
Anthropic; this plugin does not imply their endorsement.
