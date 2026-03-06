---
name: quote-manager
description: Track, compare, and manage supplier quotes. Use when Ari asks about quotes, pricing, comparisons, best price, or quote status.
---

## Instructions

### When a new quote arrives:

1. Extract from the email: supplier name, quoted price, unit of measure, lead time, MOQ, payment terms, quote validity date
2. Update quotes/quote-tracker.csv — find the matching row by supplier and part, update the fields and change status to "Quote Received"
3. Run `python3 sync_to_sheets.py` to push the updated CSV to Google Sheets
4. Update comms/[supplier-name].md with the quote details and date received
5. Notify Ari via Telegram with a short summary: "[Supplier] quoted [price] per [unit], [lead time] lead time, MOQ [quantity]"

### When Ari asks to compare quotes:

1. Read quotes/quote-tracker.csv
2. Filter to the relevant part or service
3. Present quotes as numbered card blocks sorted by price (NEVER use markdown tables — Telegram cannot render them). Use this format:

   🏭 Supplier Name
   💰 $X.XX / unit
   ⏱ Lead time: X weeks
   📦 MOQ: X units
   💳 Payment: Net 30
   📅 Valid until: YYYY-MM-DD

   Separate each quote with a blank line.
4. Highlight the best value — consider price, lead time, and MOQ together
5. Note any trade-offs: "Supplier A is cheapest but has 8-week lead time. Supplier B costs 10% more but ships in 2 weeks."

### When Ari asks for status:

1. Read quotes/quote-tracker.csv
2. Present each active RFQ/quote as a card block (NEVER use markdown tables). Use this format:

   🏭 Supplier Name
   📋 Part/Service requested
   📤 RFQ sent: YYYY-MM-DD
   📊 Status: Awaiting Response / Quote Received / etc.
   ⏱ Days waiting: X
   📝 Notes (if any)

   Separate each entry with a blank line.
3. After all entries, add a summary: "X RFQs sent, X quotes received, X need follow-up"
4. Flag any RFQs sent more than 3 days ago with no response as "needs follow-up"
5. List next actions

## CSV Format

File: quotes/quote-tracker.csv
Columns: Date, Supplier, Part/Service, Quoted Price, Unit, Lead Time, MOQ, Payment Terms, Valid Until, Status, Notes

Status values: RFQ Sent, Quote Received, Follow-up Needed, Accepted, Declined, Expired

## Rules

- Never modify old rows — update them in place
- Always keep the CSV headers intact
- After ANY change to quote-tracker.csv, run `python3 sync_to_sheets.py` to sync to Google Sheets
- If a quote seems unusually high or low compared to others, flag it for Ari
