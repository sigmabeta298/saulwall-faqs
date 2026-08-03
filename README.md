# Spend Glance FAQ Content

This repo contains the single source of truth for Spend Glance's FAQ content, consumed by:

- **Spend Glance App** — uses the `users` audience
- **Spend Glance Marketing Website** — uses the `public` audience

Content is validated and filtered using [`@saulwalltech/faq-forge`](https://www.npmjs.com/package/@saulwalltech/faq-forge).

## Editing FAQs

Edit `faq.yaml` directly. Structure:

```yaml
title: <doc title>
audiences:
  public:
    <sectionKey>:
      title: <section title>
      faqs:
        - id: <unique-id>
          question: <question text>
          answer: <answer text>
  users:
    <sectionKey>:
      ...
```

After editing, commit and push. Consuming repos (app, website) will need to pull the latest commit to see changes (see their respective READMEs for how they reference this repo).