---
layout: page
title: Projects
description: A collection of my work and side projects
permalink: /pages/projects.html
---

Here are some of the projects I've worked on:

## Iceberg Rust

**Description:** An unofficial Rust implementation of Apache Iceberg, an open table format for large analytical datasets. This project provides ACID guarantees and seamless integration with the Apache Arrow ecosystem and DataFusion query engine. It supports reading and writing Iceberg tables with partitioning, equality deletes, Iceberg views (read-only), and materialized views with full and incremental refresh options.

**Technologies:** Rust, Apache Arrow, DataFusion, Tokio, Parquet, object_store library. Supports multiple catalog backends including REST, S3Tables, Filesystem, AWS Glue, PostgreSQL, and MySQL.

**Links:** [GitHub](https://github.com/JanKaul/iceberg-rust) | [Demo](#)

---

## Frostbow

**Description:** A high-performance, in-process analytical query engine that combines Apache DataFusion with Apache Iceberg integration. Frostbow provides native support for reading and writing Iceberg tables stored in object storage, with a SQL interface that offers DataFusion SQL compatibility plus Frostbow-specific commands for table creation, data insertion, and schema management.

**Technologies:** Rust, Apache DataFusion, Apache Iceberg, S3, Google Cloud Storage. Supports multiple catalog backends including S3Tables, Filesystem, AWS Glue, and SQL catalogs.

**Links:** [GitHub](https://github.com/JanKaul/frostbow) | [Demo](#)

---

## Airberg

**Description:** A Docker-based tool that bridges Airbyte source connectors with Apache Iceberg tables. Airberg simplifies data pipeline workflows by fetching data from various Airbyte sources and loading them directly into Iceberg table formats. It uses JSON configuration files for sources and destinations, with support for environment variable substitution to enable secure credential management without hardcoding secrets.

**Technologies:** Python, Java, Docker, Gradle, Airbyte, Apache Iceberg

**Links:** [GitHub](https://github.com/dashbook/airberg) | [Demo](#)

---

