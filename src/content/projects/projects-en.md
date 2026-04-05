---
lang: en
---

## SquareSolve

I created SquareSolve at the end of university, with the goal of familiarizing myself with a few tools that I was interested in at the time. Mainly this consisted of getting the hang of Redux for state management, websockets (which I used for live multiplayer), and Firebase which I used to store some user and leaderboards data. 

[squaresolve](squaresolve.xyz)

## FinCite 

A tool that let's you dive into the financials of fortune 500 companies. The application lets you select a company and any number of its financial disclosure documents from the last 5 years. The selected documents are ingested through a custom-built RAG pipeline to generate embeddings which serve as the knowledge base. You can then ask questions about the given company and your answers will be grounded in the data from the ingested data. The filing documents that you can choose from all sourced from the SEC EDGAR api which is a filing repository run by the SEC. It holds filings from most US companies.

The main area of focus of this project was to familiarize myself with patterns for resilient services using a background job tool (in this case Hangfire). The ingestion pipeline was separated into idempotent stages that persisted the results of their work, allowing retries to resume ingestion at a given "checkpoint" instead of starting the entire pipeline from the beginning.

Although that was the main focus it also provided an opportunity to learn about working with rate limiting (from the SEC EDGAR API and  the OpenAI embeddings api), realtime streaming of updates to the frontend using sockets protocol (using SignalR), and other general data ingestion concepts.

[fincite.cc](fincite.cc)

