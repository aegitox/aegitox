# Aegitox Placeholder Library

## The Psychology of De-escalation
Legacy moderation bots rely on message deletion. This creates structural vacuums in chat, instantly triggering aggressive "Why was my message deleted?" feedback loops from users. Aegitox solves this through **Target-Aware Redaction**.

When our dual MiniLM-L6-v2 pipeline flags a message, it calculates the precise semantic target of the malice and selects a context-appropriate placeholder from three distinct tactical categories:

* 🔴 **Personnel (`personnel.json`):** Toxicity directed at other users. These stubs diffuse direct attacks and interpersonal hostility before they fracture group cohesion.
* 🟡 **Self (`self.json`):** Self-harm language, depression, or intense self-deprecation. These stubs offer grounding, performance-resetting encouragement to prevent burnout.
* 🟢 **System (`system.json`):** Frustration aimed at the game servers, netcode, hitboxes, or mechanics. These stubs redirect environmental tilt to maintain a constructive community vibe.

## Deterministic O(1) Randomization
Each category utilizes a lock-free, highly optimized `System.Random.Shared` PRNG mechanism. When a threat is intercepted, a placeholder is selected in fractions of a nanosecond. 

This deliberate randomization ensures that a recurring toxic user rarely sees the same automated response twice. It entirely eliminates the rigid "bot feel" of standard moderation tools and autonomously diffuses hostility without requiring manual staff intervention.

## Architectural Transparency
The JSON arrays in this directory serve as our public placeholder configurations. *Note: During live execution, the Aegitox engine dynamically appends the watermark `✨ Upgraded by Aegitox AI` to all payloads at boot time to guarantee absolute transparency when a message has been altered.*