# C++ Hackathon

## Problem Statement

Implement a client-server model for bulk data using Flatbuffer serialization

## Design

```mermaid
flowchart LR
((Data)) --> Client
Client --> |Send/Recieve|Server
Server --> ((Output))
```

## Getting started

Execute the flatc.exe using the below command:

```bash
.\flatc.exe --cpp .\network_Can.fbs
```

This exe takes the fbs file as input and generates "network_Can_generated.h"

Below are steps to build and execute this project:

### Using manual commands:

```bash
<Path to the g++.exe in minGW folder> -fdiagnostics-color=always -g <Path to server.cpp> -o <Output path to generate server.exe> -lws2_32
```

```bash
<Path to the g++.exe in minGW folder> -fdiagnostics-color=always -g <Path to client.cpp> -o <Output path to generate client.exe> -lws2_32
```

On executing above commands, server.exe and client.exe are available

First run the server.exe and then client.exe

The flatbuffer recieved from client can be found in network.log


### Using CMake:

The manual commands are added in CMakeLists.txt

On configuring the project, server.exe and client.exe will be available and also run automatically

NOTE: Alternatively, the above steps have already been done and executables are available in the repo

The flatbuffer recieved from the client will be stored in build/network.log 


## Tests

Gtest framework has been used to test this repo

This test will be run automatically 

## References

Gtest : http://google.github.io/googletest/quickstart-cmake.html 
Flatbuffer : https://google.github.io/flatbuffers 
