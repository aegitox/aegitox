# Enterprise Compliance & Privacy Architecture

Aegitox operates as a B2B Infrastructure Provider (Data Processor). We recognize that massive corporate guilds and enterprise communities require rigorous, uncompromising data privacy standards to satisfy GDPR, CCPA, and global digital privacy regulations. 

This document outlines the strict legal, architectural, and operational frameworks governing data transit, processing, and financial sovereignty within the Aegitox ecosystem.

## 1. Volatile Processing & Data Sovereignty
To enforce absolute data sovereignty and mitigate legal exposure, Aegitox operates on a strict zero-retention processing pipeline. 
* **Hetzner Edge Nodes:** All Level 1 deterministic routing, payload extraction, and semantic threat evaluations are executed on our primary Hetzner bare-metal edge clusters.
* **Volatile Memory Execution:** Ingress text payloads and contextual data are processed entirely within volatile RAM. 
* **Cryptographic Purging:** Contextual data is mathematically purged the exact millisecond the threat evaluation completes. Aegitox explicitly does not write chat history to physical disks, relational databases, or long-term storage volumes. No ingested text is ever used to train or fine-tune AI models.

## 2. Cloud Escalations & ZDR Architecture
Complex moderation scenarios requiring "Grey Zone" semantic analysis are routed via our PRO tier gateway. To maintain compliance during cloud escalation:
* **Priority Isolation:** Any data dynamically leaving the local Hetzner edge node is routed exclusively to OpenRouter's enterprise endpoints via a secured, ephemeral connection.
* **Zero Data Retention (ZDR):** OpenRouter operates under a legally mandated ZDR guarantee. No message content, metadata, or intermediate embeddings routed through this priority lane are ever logged, retained, or utilized by third-party subprocessors.

## 3. Financial Sovereignty & PII Liability
Aegitox explicitly decouples its core AI infrastructure from financial and consumer data liabilities.
* **Absolute Isolation:** The Aegitox core engine never touches, stores, processes, or transmits payment data, credit records, or billing-related Personally Identifiable Information (PII).
* **Authorized Merchant of Record:** All subscription transactions, global tax compliance, and financial data processing are exclusively managed by our Merchant of Record, **PayPro Global**. All legal and operational liability regarding payment security and billing PII is shifted entirely to PayPro Global's bank-level encrypted infrastructure.
