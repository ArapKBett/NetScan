# CyberTool: Network Vulnerability Scanner

A cybersecurity tool for scanning network vulnerabilities, built with C++, Java (Spring Boot), and a hacker-style web interface. Deployable on Render.

## Features
- **Port Scanning**: Uses C++ for fast TCP port scanning.
- **Web Interface**: Hacker-themed UI with animated server-style background.
- **Backend**: Java Spring Boot for processing and serving results.
- **Deployment**: Dockerized for easy hosting on Render.

## Prerequisites
- CMake, GCC (for C++ scanner)
- Maven, JDK 17 (for Java backend)
- Docker (for deployment)
- Render account

## Build and Run Locally
1. **Build C++ Scanner**:
   ```bash
   cd c++_scanner
   mkdir build && cd build
   cmake .. && make

2. Build and Run Java Backend:

```
cd java_backend
mvn clean package
java -jar target/cyber-backend-1.0-SNAPSHOT.jar```


Access at `http://localhost:8080`.

3. Build Docker Image

```docker build -t NetScan .
docker run -p 8080:8080 NetScan```

