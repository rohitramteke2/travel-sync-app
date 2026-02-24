# Data Flows

## 1. New Trip Request Flow

Step 1: User submits trip request (origin, destination, dates, team size, purpose)

Step 2: Orchestrator parses intent into structured JSON

Step 3: Policy validation executed

Step 4: Parallel agent delegation:

* Flight Agent (cost/time options)
* Hotel Agent (rate validation)
* Transport Agent (local commute estimation)
* Guide Agent (destination intelligence)

Step 5: Travel Optimization logic compares options

Step 6: Aggregated response returned to user dashboard

---

## 2. Expense Processing Flow

Capture → Classify → Validate → Store → Report

Sources:

* Booking agents (auto-import)
* Manual entry
* OCR simulation (MVP)

Classification Signals:

* Location
* Time-of-day
* Merchant category
* Policy thresholds

---

## 3. Safety Monitoring Flow

Trip Active → Monitor signals → Detect anomaly → Notify traveler → Escalate if required

---

## 4. Data Storage (MVP)

* Policy JSON
* Cost Matrix
* CRM mock dataset
* Trip records
* Expense records
