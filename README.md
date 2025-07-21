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

#c++ Scanner

`pkg install cmake`

`mkdir -p build
cd build`

`cmake ..`

`make`

termux

`cmake .. -DCMAKE_INSTALL_PREFIX=$PREFIX
make
make install`


summary

`cd ~/NetScan/c++_scanner
mkdir -p build
cd build
cmake ..
make`

usage

`./scanner 127.0.0.1 1 100`

java_backend

`pkg install openjdk-17
pkg install maven`

`cd ~/NetScan/java_backend
mvn clean package`

option 1; run directly with maven

`mvn spring-boot:run`

option 2; run packaged jar

`java -jar target/cyber-backend-1.0-SNAPSHOT.jar`

to access visit

`http://localhost:8080/`

To allow external devices on your LAN to access your backend:

In `src/main/resources/application.properties` add:

`server.address=0.0.0.0
server.port=8080`

This configures Spring Boot to listen on all interfaces, making it accessible via your local network IP address.

Find your local IP on the machine running the backend (e.g., 192.168.1.100).

Then access from other devices on the same LAN:

`http://192.168.1.100:8080/`

To expose it publicly you need tunneling services like `ngrok` or `localhost.run`.

For example, use ngrok to create a secure public URL forwarding to your local Spring Boot port.

Or use the localhost-run-spring-boot-starter dependency to generate public URLs automatically.

Access via HTTPS (Optional, Local Dev)
Spring Boot by default runs HTTP. For HTTPS:

Generate a self-signed certificate and configure your app to use it in application.properties:

`server.port=8443
server.ssl.key-store=classpath:keystore.p12
server.ssl.key-store-password=yourpassword
server.ssl.key-store-type=PKCS12
server.ssl.key-alias=tomcat`

Then use:

`https://localhost:8443/`

