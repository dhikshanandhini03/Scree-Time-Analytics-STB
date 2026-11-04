# Scree-Time-Analytics-STB
Azure pipeline for Android TV Screen Time: set-top box app events stream through Event Hubs into a Bronze/Silver/Gold lakehouse. Databricks (PySpark) removes duplicates and builds sessions and daily app usage, served from Cosmos DB by a secured FastAPI service.
