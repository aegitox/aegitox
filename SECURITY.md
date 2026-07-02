# Security Policy & Enterprise Defense Posture

Aegitox takes the security of our infrastructure, AI pipeline, and user communities as an absolute mandate. We operate under a strict Zero-Trust architecture, spanning our Cloudflare edge network, Firebase-hosted Angular v22 command center, and Hetzner backend clusters.

## Data Sovereignty & Zero Retention
Aegitox enforces absolute data sovereignty through a strict zero-retention pipeline. On our local Hetzner edge nodes, all text processing occurs exclusively in volatile memory.
* Text payloads are mathematically purged the exact millisecond the threat evaluation completes.
* We do not write chat history to disk, nor do we train AI models on user data.

## Algorithmic Supremacy & Stability
Our core processing grid is engineered in .NET 10 and hardware-accelerated C++ libraries. The backend operates on a strict $O(1)$ mandate, executing webhook intercepts, payload extraction, and memory mapping in constant time.
* The primary production edge is constrained to a 3-core, 4GB RAM allocation to actively demonstrate our execution efficiency under heavy concurrent loads.
* To prevent database locking and ensure atomic integrity, we bypass standard relational indexing overheads (such as dedicated `ActionReason` columns), extracting all necessary audit traits natively from the underlying `RawPayload` JSON.

## Threat Evaluation Accuracy
Our dual MiniLM-L6-v2 pipeline is surgically tuned for gaming and high-volume community networks. The primary Toxicity Gate (Door 1) is hardcoded to trigger exclusively at a `0.92` semantic confidence threshold. Competitive gaming banter and specific in-game context structurally fall below this threshold, ensuring they safely remain in the "Green Zone" to eliminate false positives.

## Responsible Disclosure Policy (Reporting a Vulnerability)
If you discover a security vulnerability within the Aegitox Discord bot, our interface, or the routing edge, **do not create a public issue.** Public disclosure of unpatched vulnerabilities puts our users and infrastructure at risk.

We ask that you practice Responsible Disclosure by utilizing one of our two private reporting channels:

1. **GitHub Security Advisory:** Report the vulnerability directly via the [Security Advisory Tab](https://github.com/aegitox/aegitox/security/advisories) to initiate a secure, private communication channel with our core engineering team.
2. **Direct Email:** Alternatively, email your findings directly to `support@aegitox.com` with the subject line `[SECURITY DISCLOSURE]`.

We prioritize and investigate all responsible reports immediately.
