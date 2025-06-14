# 📊 IPO Chart – Smart Home Semantic System

## ✅ INPUT
- Ontology definition file (`smart_home.owl`) from Protégé  
- IoT device metadata (e.g., ID, type, room, status)  
- Sensor readings (e.g., temperature, motion, humidity)  
- Device state (e.g., ON/OFF, triggered)  
- SPARQL query templates or user-defined queries  
- (Optional) Semantic rules (e.g., SWRL or coded logic)  
- (Optional) User actions from a UI (e.g., form or buttons)  

## 🔄 PROCESS
- Model ontology using Protégé (classes, properties, individuals)  
- Simulate IoT device behavior and generate RDF triples  
- Load and update RDF data dynamically (manual or automated)  
- Execute SPARQL queries to extract meaningful information  
- Apply logic for semantic rules or conditions (e.g., motion → light)  
- (Optional) Host ontology using Apache Jena Fuseki or GraphDB  
- (Optional) Handle UI input and route SPARQL queries from interface  

## 📤 OUTPUT
- SPARQL query results (e.g., list of active devices, room temperatures)  
- Updated ontology with current device states  
- Logs of device actions or triggered events  
- (Optional) Visual dashboard of room/device layout  
- (Optional) Real-time alerts or notifications  
