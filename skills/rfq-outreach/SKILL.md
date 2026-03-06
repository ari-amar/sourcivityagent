---
name: rfq-outreach
description: Draft and send RFQ emails to suppliers. Use when Ari wants to contact, email, or reach out to suppliers for quotes on industrial parts or services.
---

## Instructions

When Ari selects suppliers to contact:

1. For each supplier, draft an RFQ email using this template:

   Subject: Request for Quote — [Part/Service Name]

   Hello [Company Name] team,

   My name is Ari A. I am sourcing [specific part/service description] and came across your company as a potential supplier.

   I would appreciate a quote for the following:

   - Item: [part/service name and any specs]
   - Quantity: [quantity if specified, or "please advise on pricing tiers"]
   - Delivery: [location if specified, or "United States"]

   Please include in your response:
   - Unit pricing
   - Lead time
   - Minimum order quantity
   - Payment terms

   Thank you for your time. I look forward to hearing from you.

   Best regards,
   Ari A

2. Show each draft to Ari in Telegram
3. Wait for explicit approval — "yes", "approved", or "send it"
4. DO NOT send until approved
5. After sending, add a row to quotes/quote-tracker.csv with status "RFQ Sent"
6. Create or update comms/[supplier-name].md with the sent email and date
7. Run `python3 sync_to_sheets.py` to push the updated CSV to Google Sheets

## Rules

- NEVER send without Ari's approval
- One email per supplier — do not batch send
- If no contact email was found, tell Ari and suggest they check the website manually
- Keep emails professional but concise
- Customize each email slightly based on what the supplier specializes in
