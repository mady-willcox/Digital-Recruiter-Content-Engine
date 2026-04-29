# Connectors

## How tool references work

This plugin uses `~~category` as a placeholder for whatever tool the operator uses in that category. The plugin describes workflows in terms of categories rather than specific products, so any operator can run it with their preferred stack.

## Connectors for this plugin

| Category | Placeholder | Options |
|---|---|---|
| LinkedIn outreach automation | `~~LinkedIn outreach tool` | Dripify, Expandi, Waalaxy, Heyreach, or similar |

The engine itself is instruction- and knowledge-only; it does not call any external tools. The placeholder above appears once in the closing Strategy Reminder shown at the end of every session, where the operator is reminded to send 200 connection requests per week through their automation platform.
