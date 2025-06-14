# 🎯 Use Case Diagram – Smart Home Semantic System

## 📌 Purpose
This diagram shows the main interactions between users and the system, outlining the system's core functionality and the actors that interact with it.

---

## 🧍 Actors
- **Home User** – Interacts with the system via UI to monitor or control smart devices.
- **IoT Device** – Sends real-time sensor data (e.g., temperature, motion, on/off state).
- **Ontology Engine** – Stores the semantic model and current states of all devices.
- **SPARQL Interface** – Accepts and processes semantic queries.
- **Admin (Optional)** – Manages and maintains ontology data or system rules.

---

## ✅ Use Cases

| Actor         | Use Case                                         |
|---------------|--------------------------------------------------|
| Home User     | View device status                               |
| Home User     | Run semantic queries                             |
| Home User     | Simulate device actions (e.g., toggle light)     |
| IoT Device    | Send sensor readings                             |
| Ontology Engine | Update device state in ontology                 |
| SPARQL Interface | Process and return query results              |
| Admin (opt)   | View logs or modify ontology manually            |

---

## 🧭 Mermaid Diagram

```mermaid
actor User
actor "IoT Device" as Device
actor "Ontology Engine" as Onto
actor "SPARQL Interface" as SPARQL
actor Admin

User --> (View Device Status)
User --> (Run Semantic Query)
User --> (Toggle Device)

Device --> (Send Sensor Data)

(Send Sensor Data) --> Onto
(Toggle Device) --> Onto
(View Device Status) --> SPARQL
(Run Semantic Query) --> SPARQL

Admin --> (View Logs)
Admin --> (Edit Ontology)
