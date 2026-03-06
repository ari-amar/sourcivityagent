---
name: supplier-search
description: Find and evaluate US industrial suppliers. Use when Ari asks to find suppliers, vendors, manufacturers, or distributors for any industrial part, component, or service.
---

## Instructions

When Ari asks to find a supplier for a part or service:

1. Run 3-5 web searches using varied queries:
   - "[part/service] supplier USA"
   - "[part/service] manufacturer United States"
   - "[part/service] distributor wholesale US"
   - "best [part/service] company America"
2. Visit the top results and extract from each website:
   - Company name
   - City and state
   - Products or services they offer
   - Certifications (ISO, AS9100, etc.) if listed
   - Contact email (check the Contact or About page)
   - Phone number if available
3. Rank by relevance to what Ari asked for
4. Present top 3-5 options as numbered card blocks (NEVER use markdown tables — Telegram cannot render them). Use this format for each supplier:

   1️⃣ Company Name
   📍 City, State
   🔧 Products/services offered
   🏅 Certifications (if any)
   🌐 website.com
   📧 contact@email.com
   ✅ Why good match

   Separate each supplier with a blank line.
5. Ask which suppliers Ari wants to contact

## Rules

- US suppliers only unless Ari says otherwise
- Skip results that are just directories or aggregator listings with no real company info
- If no contact email is found on the website, note "email not found — check website" and include the URL
- Never contact suppliers without Ari's approval
