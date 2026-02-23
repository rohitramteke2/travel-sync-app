# System Architecture

## 1. Architectural Model

The system follows a Hub-and-Spoke Multi-Agent Architecture.

```
User Interface (Web / Dashboard)
        ↓
Backend API Layer
        ↓
Master Orchestrator Agent
        ↓
Specialized AI Agents
        ↓
Data Layer (DB + Policies + Mock APIs)
```

---

## 2. Core Components

### 2.1 Frontend Layer

* Trip request input
* Dashboard display
* Cost comparison tables
* Explanation panels

### 2.2 Backend Layer

* API Gateway (Node.js / Python)
* Agent orchestration logic
* Rule engine
* Policy validation

### 2.3 Master Orchestrator Agent

Responsible for:

* Intent parsing
* Agent selection
* Workflow sequencing
* Response aggregation

### 2.4 Specialized Agents

* Flight Agent
* Hotel Agent
* Transport Agent
* Guide Agent
* Expense Agent
* Visa Agent
* Safety Agent
* Notification Agent

Each agent functions as a modular intelligence unit.

---

## 3. Data Layer

### Data Sources (MVP Simulated)

* Travel policy JSON
* Cost matrix
* CRM mock data
* Emergency contacts database

---

## 4. Communication Model

Agent-to-agent communication uses structured JSON task objects.

Example:

```
{
  "taskId": "uuid",
  "tripId": "TRIP-001",
  "agent": "FlightAgent",
  "payload": { ... }
}
```

---

## 5. Scalability Strategy

* Modular agent architecture
* Independent deployment per agent
* Stateless request handling
* Policy-driven configuration

---

## 6. Competition Adaptation

For competition:

* APIs are simulated
* Booking calls are mocked
* Decision logic is real
* Explainability is emphasized
