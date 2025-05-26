# Financial-Document-Intelligence-Platform

## Project Directory Structure

### financial-doc-intel-platform/
```text
│
├── backend/
│   ├── api-service/              ← Spring Boot app (upload/search API)
│   │   ├── src/
│   │   ├── pom.xml
│   │   └── openapi.yaml
│   └── kafka-producer/          ← Java Kafka producer for document upload
│       ├── src/
│       └── pom.xml
│
├── parser/
│   ├── consumer/                 ← Python Kafka consumer + parser
│   │   ├── main.py
│   │   └── parser_utils.py
│   └── requirements.txt
│
├── database/
│   ├── mongo/                    ← MongoDB initialization/config
│   │   └── init.js
│   └── elasticsearch/           ← Elastic index templates
│       └── index-template.json
│
├── kafka/
│   ├── topics/
│   │   ├── doc_uploaded.json     ← Schema for uploaded doc
│   │   └── doc_parsed.json       ← Schema for parsed metadata
│   └── docker-kafka.yml          ← Docker setup for Kafka & Zookeeper
│
├── docker-compose.yml            ← Unified service runner
├── README.md
└── .env