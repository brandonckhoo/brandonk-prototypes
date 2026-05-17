# Retell Billing UI Reference

Screenshots captured 2026-05-11. Re-share originals to this folder if needed for prototyping.

---

## Page Structure

**Page header:** "Billing" with `...` overflow menu, "Change payment methods" button, "Manage billing info" button (both with external link icons).

**Two tabs:** Billing History | Usage

---

## Tab 1: Billing History

### Collapsed list columns
- Invoice Created At
- Amount
- Details
- Status (dot badge: green "Ongoing", grey "Paid")
- Invoice link (diagonal arrow icon)

### Upcoming Invoice (expanded)
Status: Ongoing | Amount: $179.65

Line items:
| Name | Amount | Details |
|---|---|---|
| Voice LLM | $16.16 | 359 minutes |
| Phone Number | $14.00 | 1 number |
| Short Call Surcharge | $17.47 | |
| LLM Token Surcharge | $25.00 | |
| Concurrency | $80.00 | 10 max limit |
| Voice Engine | $19.75 | 359 minutes |
| TTS | $5.48 | 359 minutes |
| Features | $1.79 | |

### Past invoice example — May 8, 2026 (expanded)
Amount: $500.71

Line items:
| Name | Amount | Details |
|---|---|---|
| Voice LLM | $108.14 | 2402 minutes |
| Short Call Surcharge | $32.21 | |
| LLM Token Surcharge | $136.53 | |
| Text LLM Charges | $43.34 | Note: Covers all text LLM usage, including test chat, post call analysis, chat, and simulation testing. |
| Voice Engine | $132.17 | 2402 minutes |
| TTS | $36.30 | 2402 minutes |
| Features | $12.02 | |

### Past invoice example — Apr 9, 2026 (expanded)
Amount: $501.59

Line items include all of the above plus:
| Name | Amount | Details |
|---|---|---|
| Voice LLM | $88.09 | 1958 minutes |
| Short Call Surcharge | $9.32 | |
| LLM Token Surcharge | $194.63 | |
| Text LLM Charges | $11.04 | Note: Covers all text LLM usage, including test chat, post call analysis, chat, and simulation testing. |
| Voice Engine | $107.75 | 1959 minutes |
| TTS | $78.36 | 1959 minutes |
| Features | $9.80 | |
| 2654 × Quality assurance (per second) (at $0.10 per 60 units / month) | $4.50 | 2654 × Quality assurance (per second) (at $0.10 per 60 units / month) |

Note: Quality Assurance appears as a per-second metered add-on line item with full pricing formula in the Details column.

---

## Tab 2: Usage

### KPI cards (top row, 3 cards)
- **Total Cost:** $463.46
- **Call Minutes:** 2046.25 mins
- **Average Cost Per Minute:** $0.21

**Usage Period selector** (top left, calendar icon): "May 01, 2026 – May 11, 2026"

### Left chart: Call + Chat Cost (bar chart)
- Toggle: Day | Week (pill selector)
- Day view: daily bars, y-axis $0 to ~$80, x-axis dates (May 1, May 4, May 7, May 10, May 11)
- Week view: weekly bars, y-axis $0 to ~$340, x-axis week ranges (Apr 26–May 2, May 3–May 9, May 10–May 16)
- Bar color: solid mid-blue

### Right chart: Cost by Provider (horizontal bar chart)
Providers listed top to bottom (longest bar first):
1. LLM Token Surch... (longest, dark blue)
2. Retell Voice En... 
3. LLM-gpt 4.1
4. Short Call Surch...
5. Text Testing –...
6. Platform TTS
7. Background Voic...
8. Text Testing –... (second instance)
9. ElevenLabs TTS (shortest)

### Date picker (calendar overlay)
Two-month calendar: May 2026 | June 2026
Standard range picker with highlighted selected range.

### Overflow menu (... button)
- Stop Service (red text)
- Update PO number

---

## Design Tokens (observed)

- **Font:** Inter or system-ui, same as rest of Retell console
- **Sidebar:** Standard Retell left nav, "Billing" highlighted under SYSTEM section
- **Invoice row expand:** chevron toggle (▶ collapsed, ▼ expanded), child rows indented with no left border/line
- **Status badges:** small filled circle + text ("Ongoing" green dot, "Paid" grey dot)
- **Invoice link:** diagonal arrow icon (external link pattern), right-aligned
- **Tab style:** underline active tab, same as other Retell console tabs
- **KPI cards:** large bold number, label above in small grey text, no card border (flat)
- **Chart background:** white, no gridlines visible on bar chart
