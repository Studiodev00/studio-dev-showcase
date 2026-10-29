# Architecture

Server-rendered App Router pages load typed localized content and project media. Client components implement navigation, galleries and the draft form. The contact API delegates validation, abuse controls and delivery to separate services. Provider transports are mockable; Redis coordinates quotas and duplicate handling. An optional local mail mode is a distinct local-only architecture.

```text
Localized server pages → responsive components → project galleries / draft form
Contact API → validation and abuse controls → shared state → email transport
```

## Design rationale

Long case-study narratives remain outside client bundles. Galleries retain a static fallback. Delivery fails closed when required configuration is absent. Nonce-based script policy and review-mode indexing controls are tested separately from visual behavior.

## Boundaries

RC2 is locally verified, not deployed by this work. Privacy identity/retention decisions and external Turnstile/Redis/email configuration remain pending. No real message was sent. Automated WebKit is not a physical Safari/iPhone test. The associated studiodev.dev domain could not be opened through the read-only web check on October 29; no live portfolio link is advertised.

The diagram is an explanatory abstraction of inspected source, not a deployment topology or operational runbook. [Overview](../README.md).
