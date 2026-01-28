# 🌐 HTTP Proxy Server & Caching System

A complete network communication suite implemented in **Python** using raw Sockets. This project demonstrates the core concepts of the **HTTP protocol**, including a custom Server, Client, and an intelligent **Proxy Server with Caching** capabilities.

## 🚀 Features

### 🛡️ Proxy Server
* **Traffic Interception:** Acts as an intermediary between the Client and the Server.
* **Smart Caching:** Stores server responses locally. Future requests for the same resource are served directly from the cache, significantly reducing latency and network load.
* **Access Control:** (If implemented) Filters or logs traffic passing through.

### 🖥️ HTTP Server
* **Request Handling:** Parses raw HTTP requests (GET).
* **Resource Management:** Serves static files or API responses to clients.
* **Error Handling:** Returns appropriate HTTP status codes (200 OK, 404 Not Found, etc.).

### 👤 HTTP Client
* **Custom Requests:** Generates and sends compliant HTTP packets without using high-level libraries (like `requests`).
* **Response Parsing:** Interprets headers and body content from the server.

## 🏗️ Architecture
The system operates in a 3-tier architecture:
1.  **Client:** Sends a request to the Proxy (or Server).
2.  **Proxy:** Checks if the requested resource is in the **Cache**.
    * *Hit:* Returns the cached file immediately.
    * *Miss:* Forwards the request to the Server, saves the response in the cache, and sends it to the Client.
3.  **Server:** Processes the request and returns the data.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Networking:** `socket` library (TCP/IP)
* **Tools:** Wireshark (for packet analysis and verification)

## 📂 Project Structure
```text
├── server.py       # HTTP Server implementation
├── proxy.py        # Proxy Server with Cache logic
├── client.py       # Custom HTTP Client
├── api.py          # API utility/helper functions
└── README.md       # Project documentation
