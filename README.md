# Tap for Claude

Use your Tap buyer workspace from Claude to plan media, prepare public and
private RFPs, compare supplier responses and Deals, and prepare unsent Order
drafts. Tap returns current workspace data, concise results, and links back to
the records you can access.

This bundle contains one buyer workflow skill and a remote Tap connector. It
supports Claude chat, Cowork, and Claude Code. It runs no local server, shell
hooks, or background agents.

## Connect Tap

Install the packaged Tap plugin, then open its **Connectors** tab and connect
**Tap**. Sign in to your own Tap account and authorize the buyer workspace you
want to use. Your organization may require an owner to add the connector first.
Installing the plugin alone does not connect your account.

The connector URL is `https://claude.mcp.tap.co/v1`. Use that same URL when adding
Tap as a custom connector. No API key belongs in the plugin files or a chat.

To try a packaged bundle in Claude Code:

```sh
claude --plugin-dir /path/to/tap-media
```

Open `/mcp` to connect and sign in. The skill is available as
`/tap-media:review-broadcast-campaigns`; despite its compatibility name, it
covers the supported public and private media-sourcing workflows below.

For a direct Claude Code connection without the bundled skill:

```sh
claude mcp add --transport http --scope user tap https://claude.mcp.tap.co/v1
```

## Try a task

- “Show my campaigns and flag missing details.”
- “Prepare a public RFP for this campaign without publishing it.”
- “Compare the current supplier responses, including costs and validity.”
- “Compare supplier Deals and prepare an unsent Order draft for review.”

Public RFPs support sourcing across Tap's supported media types. Private RFPs
support TV and radio. Direct-buy planning supports supplier Deals and digital
out-of-home inventory. Existing Order tracking, permitted withdrawals,
correspondence, and creative fulfillment are also supported.

## Permissions and results

Tap acts only within the connected buyer's authorized workspace. Review the
specific target and consequence before publication, external messages,
acknowledgements, or destructive changes, and use Claude's permission controls
to approve or decline. Approval to prepare a draft does not authorize sending
it. Tap still checks permissions, current versions, lifecycle rules, and retries.

The plugin cannot place Orders, record external bookings, pay suppliers, serve
ads, act as a supplier, or delete an entire workspace. Drafts and estimates do
not reserve inventory or commit spend. Review results and follow their Tap links
when you need to continue an action in Tap.

If the connector is disconnected, connect it before asking for workspace data.
If sign-in fails, retry from the connector's connection settings. If a workspace
is missing or ambiguous, sign in with the intended account and select the
appropriate workspace; contact support if access still cannot be resolved.
Empty results do not imply access to another workspace. On a stale-version or
permission error, read the current record before making another change. After
an uncertain result, check the record rather than sending the action again.

Disconnecting removes connection access; it does not delete saved Tap data.
Tap processes tool inputs and results to perform the requested work. Use the
[privacy policy](https://tap.co/privacy-policy) for data handling information.
Never share passwords, tokens, or payment credentials in a conversation.

## Support and license

Read [Tap support](https://tap.co/support), email [help@tap.co](mailto:help@tap.co),
or review the [buyer terms](https://tap.co/buyer-terms).

Copyright (c) 2026 Tap.co LLC. This bundle is proprietary; see [LICENSE](LICENSE).
The Tap name and bundled icon belong to Tap.co LLC. Public distribution of this
bundle grants no rights to Tap's backend code.
