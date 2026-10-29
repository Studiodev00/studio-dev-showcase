# Testing

Evidence date: October 29, 2026 (America/New_York). These results come from earlier recorded runs. The five-project package refresh reviewed the receipts and original-file hashes; it did not rerun application tests, lint or builds. Tests ran in isolated private copies using existing installed dependencies; no dependency reinstall was performed. JavaScript checks used Node 24.22.1.

| Check | Result |
|---|---|
| Production webpack build | PASS |
| Server suite | 68 passed |
| Chromium + WebKit compatibility suite | 4 passed; PT/EN, responsive routes, keyboard and draft behavior |
| ESLint | PASS |
| npm dependency audit | 0 reported vulnerabilities |

## Historical evidence

RC2 evidence dated October 28 records 68 server + 88 browser + 4 compatibility tests, all passing. The earlier October 29 validation reran only 68 server + 4 compatibility tests; do not sum overlapping runs. Lighthouse 13.5.0 / Chrome 156, three local runs per profile: performance median 96 mobile / 100 desktop; accessibility and best practices 100/100; SEO 69/69 with intentional noindex; LCP 2.836 s / 0.648 s, TBT 34 ms / 0 ms and CLS 0. These are historical laboratory measurements, not field performance.

## Reproducibility and limits

The source is private, so these tests cannot be run from this documentation repository. The owner retains command receipts and redacted logs separately. Tests used fixtures/mocks without production credentials. No database migration, real email or Discord operation was authorized or executed.

RC2 is locally verified, not deployed by this work. Privacy identity/retention decisions and external Turnstile/Redis/email configuration remain pending. No real message was sent. Automated WebKit is not a physical Safari/iPhone test. The associated studiodev.dev domain could not be opened through the read-only web check on October 29; no live portfolio link is advertised.

A dependency audit is a dated registry observation, not proof of exploitability or a security certification. No coverage percentage is claimed. [Overview](../README.md).
