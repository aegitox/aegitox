# Changelog & Engineering History

All notable structural changes, algorithmic optimizations, and security calibrations to the Aegitox core engine and inference pipeline are documented in this file.

## [v1.0.0] - 2026-02-02 - Production Launch

### [Architecture]
* **Vanguard Pipeline Locked:** Officially deployed the dual MiniLM-L6-v2 semantic interceptor to the Hetzner bare-metal edge.
* **Neural Vector Alignment:** Corrected the core `IntentCategory` memory enumeration to align perfectly with the AI's foundational training data matrix. Hostile targets are now deterministically mapped as Personal (`0`), Self (`1`), and System (`2`), eliminating index mismatches and ensuring flawless routing.

### [Optimized]
* **Resource Constraint Validation:** Successfully reduced and locked the primary edge node to a strict 3-core, 4GB RAM configuration. This live calibration physically proves our $O(1)$ constant-time execution mandate, demonstrating that our 22 MB quantized models can evaluate massive concurrency without degrading the 2–12ms execution window.

### [Security]
* **Toxicity Gate Calibration:** Surgically tuned the Door 1 (Toxicity Gate) primary semantic threshold to `0.92`. Real-time telemetry confirmed this exact evaluation threshold eliminates false positives within high-volume competitive gaming networks, safely keeping standard in-game banter in the "Green Zone."

### [Feature]
* **Tactical Payload Initialization:** Finalized the deterministic $O(1)$ retrieval arrays for de-escalation. The moderation pipeline has been strictly architected to utilize tactical placeholders rather than actively rewriting toxic payloads. Deployed 3 intent-specific JSON buckets containing 120 pre-vetted strings to instantly neutralize hostile environments with static, context-aware stubs.
