# CS544 P4: SQL and HDFS

**Course:** CS544 — Big Data Systems, UW-Madison (Fall 2025)

## Overview

A fault-tolerant data system consisting of an SQL server, an HDFS cluster, a gRPC server, and a client. Reads and filters data from SQL, persists it to HDFS via WebHDFS API, and continues operating even when an HDFS DataNode fails.

## Learning Objectives

- Query SQL databases with Python
- Use the WebHDFS REST API to read/write files on HDFS
- Utilize PyArrow for efficient data serialization
- Build fault-tolerant pipelines that handle DataNode failures

## Architecture

```
SQL Server ──► gRPC Server ──► HDFS Cluster (3 DataNodes)
                   │
                   ▼
               gRPC Client
```

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Hadoop](https://img.shields.io/badge/Hadoop-66CCFF?style=flat&logo=apachehadoop&logoColor=black)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=flat&logo=google&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

## Project Structure

```
p4/
├── docker-compose.yml  # SQL + HDFS + gRPC containers
├── server.py           # gRPC server: SQL → HDFS pipeline
├── client.py           # gRPC client
├── hdfs.proto          # Protobuf definitions
└── README.md
```

## Author

**Rakshith Sriraman Krishnaraj** · MS CS @ UW-Madison · [LinkedIn](https://www.linkedin.com/in/rakshith-s-k-95b550151/)
