# Retell Connect Prototypes Index

Maps each PRD row (from Section 3.1) to its prototype file. Use this to track which screens are done, need iteration, or are covered by the designer's existing prototypes.

## Status Key
- **Done** — Mockup generated and approved
- **Draft** — Mockup generated, needs review
- **Needs new** — No prototype yet, needs to be created
- **Reuse designer** — Designer's existing prototype covers this

---

## 3.1.1 Integration Library

| # | Screen | File | Status |
|---|--------|------|--------|
| 1 | Sidebar nav (Integrations under SYSTEM) | Reuse designer | Reuse designer |
| 2 | Integrations page (with connections) — card rows with Connect/Update/Disconnect | Reuse designer | Reuse designer |
| 3 | Integrations page (empty state) | `3.1.1-integrations-empty.html` | Needs new |
| 4 | Add Integration modal (category sidebar + card grid) | `3.1.1-add-integration-modal.html` | Needs new |

## 3.1.2 Connect an Integration

| # | Screen | File | Status |
|---|--------|------|--------|
| 5 | OAuth authorization popup (HubSpot example) | Reuse designer | Reuse designer |
| 6 | Credential-based auth form (Salesforce Connected App) | `3.1.2-credential-auth.html` | Needs new |
| 7 | CRM post-auth setup (field mapping) | Reuse designer | Reuse designer |
| 8 | Integration actions (Tools list) | `3.1.2-tools-list.html` | Needs new |
| 9 | Re-auth error state | `3.1.2-reauth-error.html` | Needs new |
| 10 | Connection ownership (Created by column) | `3.1.2-connection-ownership.html` | Needs new |

## 3.1.3 Integration App Pages

| # | Screen | File | Status |
|---|--------|------|--------|
| 11 | Integration app page (Overview tab) | `3.1.3-app-overview.html` | Needs new |
| 12 | Integration app page (Settings tab) | `3.1.3-app-settings.html` | Needs new |
| 13 | Integration app page (Activity Log tab) | `3.1.3-app-activity-log.html` | Needs new |
| 14 | Error states (field, integration, workspace levels) | `3.1.3-error-states.html` | Needs new |

## 3.1.4 Integration App Template

| # | Screen | File | Status |
|---|--------|------|--------|
| 15 | Sync Contacts Data modal (field mapping) | Reuse designer | Reuse designer |
| 16 | CRM sync timing settings | `3.1.4-sync-timing.html` | Needs new |
| 17 | Non-CRM integration template (Cal.com / Slack / Zendesk config) | `3.1.4-non-crm-config.html` | Needs new |

## 3.1.5 Integration as Tool/Node

| # | Screen | File | Status |
|---|--------|------|--------|
| 18 | Agent Builder: Single Prompt (Functions panel with integration tools) | Reuse designer | Reuse designer |
| 19 | Agent Builder: Conversational Flow (Integration node on canvas) | Reuse designer | Reuse designer |
| 20 | Tool configuration panel (per action) | `3.1.5-tool-config.html` | Needs new |
| 21 | Pre-call and post-call hooks (agent settings) | `3.1.5-hooks.html` | Needs new |

---

## Summary

| Status | Count |
|--------|-------|
| Reuse designer | 8 |
| Needs new | 13 |
| **Total** | **21** |

## Generation Order (suggested)

Start with the screens that tell the core story first:

1. `3.1.1-integrations-empty.html` — First thing a user sees
2. `3.1.1-add-integration-modal.html` — How they browse and pick
3. `3.1.2-credential-auth.html` — SFDC connect flow
4. `3.1.2-tools-list.html` — What actions are available
5. `3.1.3-app-overview.html` — Post-connect management
6. `3.1.3-app-settings.html` — Edit config
7. `3.1.3-app-activity-log.html` — Monitor sync health
8. `3.1.3-error-states.html` — Error handling
9. `3.1.4-sync-timing.html` — Real-time vs scheduled
10. `3.1.4-non-crm-config.html` — Cal.com / Slack / Zendesk
11. `3.1.5-tool-config.html` — Per-action config in agent builder
12. `3.1.5-hooks.html` — Pre/post-call hooks
13. `3.1.2-reauth-error.html` — Token expiry flow
