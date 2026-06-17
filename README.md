# C Network Systems Components

A C-based systems programming project that implements basic networking components on Linux, including a client, server, proxy, and DNS client. The project focuses on socket programming, process-level networking, request forwarding, DNS lookup behavior, and reliable command-line software design.

## Overview

This repository demonstrates core systems and network programming concepts in C. The project includes multiple components that communicate over the network and model common infrastructure patterns such as client-server communication, proxy forwarding, and DNS resolution.

The goal of the project is to build a stronger understanding of how low-level networking software works beneath higher-level web and application frameworks.

## Key Features

* Client-server communication in C
* Proxy-style request forwarding
* DNS client / lookup functionality
* Socket programming on Linux
* Command-line based execution
* Manual request and response handling
* Error checking and debugging for network programs
* Modular C source files for separate networking components

## Technical Topics

This project demonstrates experience with:

* C programming
* Linux systems programming
* TCP/IP networking concepts
* Socket APIs
* Client-server architecture
* Proxy behavior
* DNS lookup workflow
* Command-line tools
* Debugging low-level network behavior

## Repository Structure

```text id="23sbdv"
.
├── DNS_client_*.c      # DNS client / lookup component
├── client_*.c          # Network client implementation
├── server_*.c          # Network server implementation
├── proxy_*.c           # Proxy / forwarding component
└── README.md
```

The exact file names may include team member names or course-specific suffixes, but the main components are organized around client, server, proxy, and DNS-client functionality.

## How It Works

The project is divided into several networking components.

### Client

The client sends requests to a server or proxy and receives responses over a network socket. This component demonstrates how user-level programs initiate network communication.

### Server

The server listens for incoming connections, accepts client requests, and sends responses. This component demonstrates how services expose network functionality through sockets.

### Proxy

The proxy sits between a client and server. It receives a client request, forwards it to the destination server, receives the response, and sends the response back to the client. This helps demonstrate how intermediaries work in networked systems.

### DNS Client

The DNS client component demonstrates how domain-name lookup works at a lower level. It helps connect human-readable hostnames with network addressing concepts.

## Build

Compile each C file with GCC. For example:

```bash id="c5ijwj"
gcc -Wall -Wextra -o server server_*.c
gcc -Wall -Wextra -o client client_*.c
gcc -Wall -Wextra -o proxy proxy_*.c
gcc -Wall -Wextra -o dns_client DNS_client_*.c
```

Depending on the exact filenames and dependencies, you may need to adjust the compile commands.

## Example Usage

Start the server:

```bash id="5jdkor"
./server
```

Run the client:

```bash id="id2r28"
./client
```

Run the proxy:

```bash id="h48kvi"
./proxy
```

Run the DNS client:

```bash id="6xgvc8"
./dns_client
```

Command-line arguments may vary depending on the implementation. Check the source files for required host, port, or query parameters.

## What I Learned

This project strengthened my understanding of how networking systems work at the C and operating-system interface level. Instead of relying on high-level networking libraries, I worked directly with lower-level networking concepts such as sockets, request forwarding, client-server communication, and DNS behavior.

The project also improved my ability to debug C programs, reason about data flow between processes, and understand how infrastructure components communicate over a network.

## Future Improvements

* Add a Makefile for easier compilation
* Add clearer command-line argument handling
* Add logging for requests and responses
* Add timeout and retry handling
* Add support for multiple concurrent clients
* Add more detailed test cases
* Add diagrams showing client, proxy, server, and DNS flow

## Author

Xiang Mao
B.S. Computer Engineering, University of California, Davis
GitHub: https://github.com/XiangM7
LinkedIn: https://www.linkedin.com/in/xiang-mao-78ab73301/
