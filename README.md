# Mutadata

> 🧬 **Clean, Transform & Enrich your data with one simple API**  
> Your programmable Swiss Army knife for structured data.

---

**Mutadata** is a programmable API that lets you manipulate, clean, and enrich your structured data — starting with JSON, and soon expanding into CSV, plain text, and AI-powered enrichments. Whether you're cleaning messy inputs, rewriting field names, or preparing data for ML — Mutadata gives you building blocks you can automate.

⚡ Built for developers.  
🔧 Flexible by design.  
🧠 Getting smarter by the day.

---

## ✅ What it can do today

You can already call the API to:

- 🧪 **Copy fields** — duplicate data across your structure
- 🧹 **Remove empty values** — clean up nulls, empty strings, arrays, and objects
- 🏷️ **Rename fields** — simple refactoring of your JSON keys

---

## 🧪 Try it now (API is live!)

The API is live and free to test — no auth needed for now.

> 👉 Visit the [site](https://mutadata.giox.tech) or test it directly using curl (see below).

### 🧾 Example: JSON request

```bash
curl -X POST https://mutadata-api.giox.tech/transform/json \
  -H "Content-Type: application/json" \
  -d '{
    "operations": [
      {
        "copy": {
          "field_dst1": "field_src1",
          "field_dst2": "field_src2"
        }
      },
      {
        "rename": [
          {"field1": "new_field1"},
          {"field2": "new_field2"}
        ]
      },
      {
        "remove_empty": {
          "strings": true
        }
      }
    ],
    "data": {
      "field1": "keep me",
      "field2": "",
      "field_src1": "copy this",
      "field_src2": "and this"
    }
  }'
```

---

## 🌱 What’s coming next

We’re actively working on:

### 🔧 Core JSON/CSV Transformations
- [ ] Flatten deeply nested fields
- [ ] Map/restructure to new schemas
- [ ] Change field formats (camelCase, snake_case, etc.)
- [ ] CSV support: filter rows, clean cells, rename columns

### 🤖 AI-Powered Enrichment (Coming Soon)
- [ ] Summarize text content
- [ ] Rephrase or rewrite in a chosen tone
- [ ] Correct grammar and spelling
- [ ] Detect sentiment, trends, or outliers
- [ ] Categorize or tag based on custom rules
- [ ] Generate statistical summaries

---

## 🧠 Why Mutadata?

You're a developer. You could build this in-house.

But should you?

Building and maintaining reliable, tested, secure data transformation code across formats, edge cases, and schema changes is a pain. With Mutadata, you can:

- Replace brittle scripts and copy-paste logic
- Test and scale data workflows without devops
- Connect to APIs, files, or databases easily
- Get new capabilities instantly as we grow

> Like `jq`, but on steroids — and available via URL.

---

## 🏁 Roadmap

> Help shape the future — [open an issue](https://github.com/gioxtech/mutadata-docs/issues) or suggest a feature!

### Core
- [x] Copy fields
- [x] Remove empty values
- [x] Rename fields
- [ ] Flatten objects
- [ ] Map fields to new structure
- [ ] Change case format
- [ ] CSV support

### Enrichment
- [ ] Summarize
- [ ] Rephrase
- [ ] Grammar check
- [ ] Sentiment analysis
- [ ] Categorize or tag
- [ ] Trend detection

---

## 🧭 About

Mutadata is a project by [Giox Technology GmbH](https://giox.tech) — built with developers and data engineers in mind.

No accounts needed (yet).  
No cost (yet).  
Just clean, programmable data power.

---

**👉 Stay tuned** — we’ll soon release a playground, dashboard, and public roadmap.

Got feedback? [Open an issue](https://github.com/gioxtech/mutadata-docs/issues), or email us at `support@giox.tech`.
