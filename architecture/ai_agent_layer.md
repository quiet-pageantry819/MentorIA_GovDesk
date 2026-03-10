# AI Agent Layer & RAG Knowledge System

<div align="center">
  <img src="../assets/rag_agent_concept.png" alt="RAG & Agent Concept" width="80%">
  <p><em>RAG & Agent Concept</em></p>
</div>

This document outlines the intelligence and execution core of MentorIA GovDesk.

## Retrieval Augmented Generation (RAG) System

To prevent hallucination and ensure absolute compliance with the law, MentorIA GovDesk relies on a robust RAG architecture.

*   **Ingestion Pipeline:** Municipal laws, ordinances, internal SOPs (Standard Operating Procedures), and public service catalogs are ingested, chunked, and vectorized.
*   **Vector Database:** Serves as the authoritative source of truth.
*   **Contextual Retrieval:** When a citizen asks a question (e.g., "How do I get a building permit?"), the system fetches the *exact* regulatory text and procedural steps before generating a response.

## Agent Orchestration & Workflow Automation

MentorIA GovDesk transcends basic Q&A by employing **Agentic AI**. Agents are given specific tools and goals to complete administrative workflows.

*   **Intent Classification Agent:** Determines if the user needs information, wants to start a process, or needs an update on an existing case.
*   **Workflow Execution:** Based on intent, the orchestration layer triggers actions:
    *   *Information Gathering:* Prompting the user for necessary data (ID number, address).
    *   *Validation:* Checking provided data against simple rules or external APIs.
    *   *Action:* Submitting an API payload to the municipal ticketing system.
*   **Auditable Decision Trails:** Every step the agent takes, the retrieved context it used, and the action it executed is logged securely for auditability and debug tracing.

## Analytics for Public Service Demand

The agent layer generates rich telemetry.

*   **Friction Detection:** If users frequently abandon the conversational flow at the "upload proof of residence" step, the analytics dashboard flags this as a procedural bottleneck.
*   **Demand Forecasting:** Identifying spikes in specific service requests (e.g., tax inquiries near deadlines) to help municipalities allocate human resources effectively.

---
**[⬅️ Back to Architecture Overview](overview.md)** | **[Next: Integrations ➡️](integrations.md)**
