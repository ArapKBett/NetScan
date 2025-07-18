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

2. Build Java Backendbash

```bash
cd backend
mvn clean install
java -jar target/cybertool-backend.jar```

3. Run Web InterfaceEnsure the backend is running.
Navigate to the frontend directory and follow the instructions in its README (e.g., serve the static files using a web server like Nginx or Node.js).

4. Docker Setupbash

```bash
# Build Docker image
docker build -t cybertool .

# Run Docker container
docker run -p 8080:8080 cybertool```

