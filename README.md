# Distributed Hash Tables (DHTs) with Chord & Pastry (Using Docker)

## Project Overview

This project was developed as part of my university coursework on **Decentralized Data Technologies**. It involves the **implementation and experimental evaluation** of **Distributed Hash Tables (DHTs)**, specifically the **Chord and Pastry** protocols. The goal is to explore the efficiency of decentralized data structures for storing and retrieving key-value pairs while utilizing **Docker containers, multi-threading, and socket communication**.

The project follows the objectives outlined in the **Decentralized Data Engineering and Technologies** course, focusing on:
- **Implementation and performance evaluation** of fundamental operations: Insert key, Delete key, Update key, Lookup (key), Node Join, and Node Leave.
- **Use of Docker and Containers** to simulate a realistic cloud-based distributed system.
- **Comparison of Chord and Pastry DHTs** based on the number of hops required for each operation.
- **Utilization of the Coffee Reviews Dataset** to evaluate query efficiency in a real-world scenario.
- **Experimental benchmarking of distributed lookups and retrieval speeds.**

## Features

- **Implementation of Chord and Pastry DHTs** for efficient key-value storage
- **Decentralized peer-to-peer architecture** with no central authority
- **Multi-threaded environment** for handling multiple requests concurrently
- **Dockerized deployment** for scalable and isolated execution
- **Experimental performance evaluation** of key operations such as insert, lookup, delete, node join, and node leave
- **Use of real-world dataset** (Coffee Reviews Dataset) for testing and benchmarking

## Technologies Used

- **Python** (for implementing Chord & Pastry DHTs)
- **Docker & Docker Compose** (for containerized execution)
- **Sockets & Multi-threading** (for distributed communication between nodes)
- **Pandas** (for dataset processing)

## Project Structure

```
│── chord.py               # Implementation of the Chord protocol
│── pastry.py              # Implementation of the Pastry protocol
│── docker-compose.yml     # Docker configuration for multi-node deployment
│── Dockerfile             # Image setup for running nodes in containers
│── coffee_analysis.csv    # Dataset used for experimental evaluation
│── report.pdf             # Detailed analysis of the project and findings
```

## Running the Project

### 1️⃣ Using Docker (Recommended)

To deploy the Chord and Pastry DHTs using Docker, follow these steps:

1. **Build the Docker image:**
   ```sh
   docker-compose build
   ```
2. **Start the distributed network:**
   ```sh
   docker-compose up
   ```
3. The system will launch multiple Chord & Pastry nodes in separate containers.
4. Check logs for performance metrics and node interactions.

### 2️⃣ Running Locally (Without Docker)

If you prefer to run the system manually:

```sh
python chord.py
python pastry.py
```

Ensure that multiple instances are executed to simulate a real peer-to-peer network.

## Experimental Evaluation

The project evaluates the performance of **Chord vs Pastry** by measuring the execution time for:

- Data insertions
- Key lookups
- Key deletions
- Node joins & departures

Results indicate that **Chord generally performs better** in terms of lookup efficiency for this specific dataset.

## Project Report

A detailed **analysis and evaluation** of this project is available in the `report.pdf` file, covering:

- Performance comparison between Chord & Pastry
- Graphical analysis of time complexity
- Discussion on scalability & fault tolerance
- Experimental findings on lookup, deletion, and insertion speeds
- Evaluation of distributed network efficiency using Docker

## Future Improvements

- **Kubernetes integration** for dynamic scaling
- **Additional optimizations** in routing efficiency
- **Enhanced fault tolerance** by implementing replication mechanisms


