---
name: comms-manager
description: Track and manage all supplier communications. Use when Ari asks about communication history, status with a supplier, or wants to follow up, reply, or negotiate with a supplier.
---

## Instructions

### When Ari asks about a supplier's status or history:

1. Read comms/[supplier-name].md
2. Summarize the timeline: first contact date, what was requested, any quotes received, last communication, current status
3. Keep the summary concise — dates and key facts only

### When Ari wants to follow up:

1. Check comms/[supplier-name].md for the last email sent
2. Draft a polite follow-up email referencing the original RFQ
3. Show the draft to Ari and wait for approval
4. Only send after approval
5. Update comms/[supplier-name].md with the follow-up

### When Ari wants to negotiate:

1. Review the quote and any competing quotes
2. Draft a negotiation email — professional, factual, referencing specific numbers
3. Show draft and wait for approval
4. Update comms log after sending

### When Ari wants to accept a quote or place an order:

1. Draft an acceptance email confirming: item, quantity, agreed price, lead time, payment terms
2. Show draft and wait for approval
3. Update quote-tracker.csv status to "Accepted"
4. Update comms log

## Communication Log Format

Each supplier gets one file: comms/[supplier-name].md
Use lowercase and hyphens for filenames — example: comms/acme-industrial.md

Format:
```
# [Company Name]
Website: [url]
Contact: [email]

## [Date] — RFQ Sent
[copy of email sent]

## [Date] — Quote Received
[summary of quote]

## [Date] — Follow-up Sent
[copy of follow-up]
```

## Rules

- NEVER send any email without Ari's approval
- Always update the comms log after every interaction
- Keep logs factual — no opinions about suppliers in the logs
- If a supplier hasn't responded in 5+ days, suggest a follow-up when Ari asks for status
