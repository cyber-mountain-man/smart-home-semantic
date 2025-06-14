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

## 🧭 Use Case Representation with Mermaid

```mermaid
graph TD

HomeUser([Home User])
IoTDevice(["IoT Device"])
OntologyEngine(["Ontology Engine"])
SPARQLInterface(["SPARQL Interface"])
Admin([Admin])

HomeUser -->|View| ViewStatus[View Device Status]
HomeUser -->|Run| RunQuery[Run Semantic Query]
HomeUser -->|Toggle| ToggleDevice[Toggle Device]

IoTDevice --> SensorData[Send Sensor Data]

SensorData --> UpdateOntology[Update Ontology]
ToggleDevice --> UpdateOntology
ViewStatus --> QueryOntology[Query Ontology]
RunQuery --> QueryOntology

Admin --> ViewLogs[View Logs]
Admin --> EditOntology[Edit Ontology]
