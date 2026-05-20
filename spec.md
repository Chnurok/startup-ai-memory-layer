# AI Memory Layer for Teams

## Product Summary

AI Memory Layer for Teams is a B2B SaaS platform that gives companies a shared, structured memory for work done across chats, calls, documents, CRM records, and internal tools. The product turns fragmented team knowledge into an operational memory that AI agents and human teams can search, reuse, and act on.

Core promise: important context should not disappear between messages, meetings, employees, or tools.

## Problem

Teams lose context constantly:

- Decisions are buried in Telegram, Slack, email, and meeting notes.
- New employees take too long to ramp up.
- AI assistants answer without enough company context.
- Sales, ops, and support repeat work because past knowledge is not reusable.
- Knowledge bases become stale because nobody wants to maintain them manually.

The result is slow execution, duplicated effort, and weak AI adoption.

## Product Vision

Build a memory infrastructure layer for modern teams:

- Automatically capture important context from daily workflows.
- Convert raw activity into structured memory units.
- Make those memory units searchable, explainable, and permission-aware.
- Feed relevant context back into humans, copilots, and automations at the moment of work.

This is not just a note-taking app and not just RAG over documents. It is a persistent memory system for teams.

## Target Users

Primary:

- Small and mid-sized remote teams
- Agencies
- Startup operations teams
- Customer success / support teams
- Sales teams with long deal cycles

Secondary:

- Professional services firms
- Internal AI platform teams
- Knowledge-heavy founder-led businesses

## Core Use Cases

1. Team memory search
Find prior decisions, commitments, client context, and process history across all integrated systems.

2. AI context injection
Provide company-specific memory to internal copilots, support bots, sales assistants, and workflow agents.

3. Automatic meeting memory
Turn calls and voice notes into structured decisions, tasks, blockers, and follow-ups.

4. Account memory
Maintain persistent memory per client, lead, vendor, or project so context accumulates over time.

5. Onboarding acceleration
Give new hires a reliable way to understand how the team actually works.

## MVP Scope

### Inputs

- Slack / Telegram export or live sync
- Meeting transcripts
- Internal docs and notes
- CRM records
- Manual notes via web UI

### Memory Pipeline

- Ingest raw events and documents
- Chunk and classify content
- Extract entities, decisions, tasks, and facts
- Link memory objects to people, accounts, projects, and topics
- Score importance and freshness
- Store with source references and timestamps

### Retrieval Layer

- Semantic search
- Filter by workspace, person, account, project, source, date
- Timeline view of memory per entity
- Answer generation with citations
- "What should I know before this meeting?" briefing

### UI

- Workspace dashboard
- Global search
- Account / project memory pages
- Meeting memory pages
- AI chat with grounded answers
- Admin permissions panel

## Key Product Features

### 1. Memory Objects

Atomic units such as:

- Fact
- Decision
- Task
- Risk
- Preference
- Relationship
- Open question

### 2. Memory Graph

Link memory objects to:

- People
- Teams
- Clients
- Deals
- Projects
- Documents
- Meetings

### 3. Context Engine

Given a prompt or workflow, retrieve the most relevant memory bundle using:

- semantic similarity
- recency
- source trust
- entity relevance
- role-based access

### 4. Memory Health

Show what is stale, conflicting, underused, or missing.

### 5. Human-in-the-Loop Controls

Users can confirm, edit, merge, reject, or pin important memories.

## Differentiation

Why this is stronger than a generic knowledge base:

- Memory is created from work, not manually maintained from scratch.
- Retrieval is entity-aware, not just document-aware.
- The system is designed for AI agent consumption, not only for humans.
- It tracks decision history and context evolution over time.
- It can become the shared context layer across multiple tools.

## Technical Architecture

### Frontend

- Web app for search, review, and workspace management

### Backend

- Ingestion workers
- Extraction / classification pipeline
- Vector + relational storage
- Retrieval / ranking service
- API for internal and third-party AI agents

### Suggested Stack

- Frontend: Next.js
- Backend: Node.js or Python service mix
- Database: Postgres
- Vector store: pgvector or dedicated vector DB
- Queue: Redis / BullMQ
- LLM layer: OpenAI-compatible APIs
- Speech input: Whisper-compatible transcription

## Non-Functional Requirements

- Workspace-level isolation
- Role-based access control
- Source citations in all AI answers
- Audit trail for memory creation and edits
- GDPR-aware deletion and retention controls
- Fast search response for normal interactive use

## Monetization

Primary model:

- SaaS subscription per workspace with seat and usage tiers

Possible expansion:

- API pricing for agent access
- Premium connectors
- Enterprise security / compliance features
- Vertical packages for agencies, sales teams, support teams

## Why It Fits the Founder

- Strong fit with existing AI, automation, transcription, and workflow background
- Can be prototyped quickly with current tooling
- Easy to demo with a believable end-to-end flow
- Can start with one narrow wedge and expand into a broader platform

## ENISA / Startup Narrative Angle

Strong points for a startup application:

- Clear technology component
- Scalable SaaS model
- B2B orientation
- Expansion potential beyond Spain
- Innovation angle around team memory infrastructure for AI-native organizations

Recommended wording:

"A shared memory infrastructure platform that converts fragmented operational knowledge into structured, permission-aware context for teams and AI agents."

## 6-Week MVP Plan

1. Week 1: Define schema, ingestion model, and first UX flows
2. Week 2: Build ingestion for transcripts, docs, and manual notes
3. Week 3: Build extraction pipeline for decisions, tasks, and facts
4. Week 4: Ship search, citations, and entity memory pages
5. Week 5: Add AI chat with contextual retrieval
6. Week 6: Polish demo workspace, sample datasets, and landing page

## Demo Scenario

A small agency uploads meeting transcripts, sales notes, and client docs. Before a client call, the system produces a short briefing:

- latest decisions
- unresolved blockers
- client preferences
- commitments already made
- suggested next steps

The user can inspect the source trail behind every memory item.

## Version 2 Ideas

- Browser / CRM / helpdesk live connectors
- Personal memory + team memory split
- Proactive reminders based on memory gaps
- Cross-workspace benchmarking
- Workflow triggers from memory changes
- Agent SDK for external tools
