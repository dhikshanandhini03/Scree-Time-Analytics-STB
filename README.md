# Scree-Time-Analytics-STB
Azure pipeline for Android TV Screen Time: set-top box app events stream through Event Hubs into a Bronze/Silver/Gold lakehouse. Databricks (PySpark) removes duplicates and builds sessions and daily app usage, served from Cosmos DB by a secured FastAPI service.

<img width="1440" height="245" alt="image" src="https://github.com/user-attachments/assets/ab832411-1efa-46ef-b1de-c3dc2016540b" />
**Capture:** set-top boxes send app start and end events to Azure Event Hubs.

**Bronze:** the ingestion service validates events, stores them raw in ADLS Gen2, and dead-letters bad ones.

**Silver:** Databricks removes duplicates and builds sessions, handling late and missing events.

**Gold:** sessions become daily usage per app, with system apps grouped under "Others".

**Serving:** Cosmos DB stores the results and a secured FastAPI service sends them to the TV.


