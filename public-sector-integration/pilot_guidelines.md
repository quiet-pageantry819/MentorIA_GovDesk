# Municipal Pilot Guidelines

Local governments interested in adopting MentorIA GovDesk will follow a structured rollout framework to minimize risk and maximize early impact.

## Phase 1: Procedural Mapping & Ingestion
1.  **Identify High-Friction Services:** Select 2-3 specific procedures (e.g., requesting a birth certificate, reporting infrastructure damage).
2.  **Document Collection:** Gather all relevant ordinances, forms, and instruction manuals.
3.  **Vectorization:** Ingest these documents into the municipal RAG partition.

## Phase 2: "Read-Only" Q&A Deployment
1.  **Soft Launch:** Deploy the AI strictly as an information retrieval agent. It will answer questions about the selected services based purely on the documents, with no ability to create tickets.
2.  **Monitoring:** Analyze the questions asked to refine the document retrieval accuracy.

## Phase 3: Agentic Orchestration Activation
1.  **API Integration:** Connect the agent layer to the specific backend system (e.g., municipal CRM).
2.  **Workflow Activation:** The agent begins actively validating user input and creating formal records.
3.  **Human in the Loop (HITL):** During the initial pilot, all AI-generated tickets are routed for manual review before entering the formal bureaucratic queue.

---
**[⬅️ Back to README](../README.md)**
