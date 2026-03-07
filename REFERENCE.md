# Quick Reference - Sourcer 📦

## Correct Himalaya Email Command

The working format for sending email via Himalaya (as of 2026-03-01):

```bash
cat << 'EOF' | himalaya template send
From: a76646325@gmail.com
To: recipient@email.com
Subject: Subject Line

Message body here
EOF
```

**Why this works:**
- Uses heredoc to pass multi-line template to stdin
- Headers (From/To/Subject) come first
- Blank line separates headers from body
- No `-H` flags needed

**Example:**
```bash
cat << 'EOF' | himalaya template send
From: a76646325@gmail.com
To: recipient@email.com
Subject: Hi

Hello,

Just reaching out to say hello.

Best regards,
Ari A
EOF
```

Output on success: "Message successfully sent!"
