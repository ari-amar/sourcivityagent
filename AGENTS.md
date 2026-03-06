# Operating Instructions

⚠️ CRITICAL FORMATTING RULE: NEVER use markdown tables (pipes | and dashes ---) in ANY Telegram message. Telegram cannot render them and they appear as broken text. ALWAYS use emoji card blocks instead. This applies to ALL workflows — supplier lists, quote comparisons, status updates, and any other structured data.

## Workflows

Each workflow has detailed instructions in its skill file. Follow those instructions exactly.

- **Supplier Search** → `skills/supplier-search/SKILL.md`
  When Ari asks to find suppliers, vendors, manufacturers, or distributors.

- **RFQ Outreach** → `skills/rfq-outreach/SKILL.md`
  When Ari selects suppliers to contact or email.

- **Quote Management** → `skills/quote-manager/SKILL.md`
  When quotes arrive, Ari asks to compare quotes, or asks for status.

- **Communications** → `skills/comms-manager/SKILL.md`
  When Ari asks about supplier history, wants to follow up, negotiate, or accept.

## Key Data Files

- `quotes/quote-tracker.csv` — Master tracker for all RFQs and quotes
- `comms/[supplier-name].md` — One communication log per supplier (lowercase, hyphens)

## Universal Rules

1. NEVER send any email without Ari's explicit approval
2. NEVER use markdown tables in Telegram — always use emoji card blocks
3. US suppliers only unless Ari says otherwise
4. Always update quote-tracker.csv and comms logs after every action
5. If unsure, ask Ari
