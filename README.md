# AI-Finance-agent-on-Graph-database-
A 3 layer system, consisting of a automated orcheastration via Airflow, connected to a central neo4j database that is queried by an AI agent built on n8n



AI Financial Analyst

An AI-powered financial analysis chatbot that combines Neo4j, n8n, Claude, Apache Airflow and Python to allow users to query investment data using natural language.

System Architecture

How it works

1. Automated data ingestion

Apache Airflow orchestrates a Python ETL process that retrieves stock-market data from the Yahoo Finance API and updates the Neo4j knowledge graph.

2. Knowledge graph

Neo4j stores investment information as interconnected nodes and relationships, allowing financial entities and their relationships to be queried efficiently.

3. AI financial agent

When a user asks a financial question, Claude translates the natural-language request into a Cypher query.

4. Query & response

The query is executed against Neo4j, with the resulting data passed back to the AI agent to generate a natural-language response.

Example

User: Which city has the highest exposure to crashing technology stocks today?

Natural language
       ↓
Claude
       ↓
Cypher query
       ↓
Neo4j
       ↓
Financial data
       ↓
Claude
       ↓
Natural-language answer
Demo

[YouTube demonstration] -  https://www.youtube.com/watch?v=kQY8w8PyT7Q


                 ┌──────────────────────┐
                 │    Yahoo Finance     │
                 │         API          │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │  Python ETL Script   │
                 └──────────┬───────────┘
                            │
                    Orchestrated by
                            │
                            ▼
                 ┌──────────────────────┐
                 │    Apache Airflow    │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │        Neo4j         │
                 │   Knowledge Graph    │
                 └──────────┬───────────┘
                            │
                     Cypher Query
                            │
                            ▲
                 ┌──────────┴───────────┐
                 │      n8n + Claude    │
                 │     AI Financial     │
                 │        Agent         │
                 └──────────┬───────────┘
                            │
                            ▼
                         User
<img width="1972" height="898" alt="image" src="https://github.com/user-attachments/assets/5446e911-014e-4059-bf8c-3726db86fd7a" />

