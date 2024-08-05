# Football Data Engineering

This Python-based project Scraping Stadiums data from Wikipedia using Apache Airflow, cleans it and pushes it Azure Data Lake for processing.

## Table of Contents

1. [System Architecture](#system-architecture)
2. [Requirements](#requirements)
3. [Getting Started](#getting-started)
4. [Running the Code With Docker](#running-the-code-with-docker)
5. [How It Works](#how-it-works)
6. [Video](#video)

## Requirements
- Python 3.9
- Docker
- PostgreSQL
- Apache Airflow 2.6
- Vagrant

## How It Works
1. Fetches data from Wikipedia.
2. Cleans the data.
3. Transforms the data.
4. Pushes the data to Azure Data Lake.
