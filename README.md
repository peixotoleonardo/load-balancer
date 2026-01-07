# Load Balancer

This challenge is to build your own application layer load balancer.

A load balancer performs the following functions:

- Distributes client requests/network load efficiently across multiple servers
- Ensures high availability and reliability by sending requests only to servers that are online
- Provides the flexibility to add or subtract servers as demand dictates

Therefore our goals for this project are to:

- Build a load balancer that can send traffic to two or more servers.
- Health check the servers.
- Handle a server going offline (failing a health check).
- Handle a server coming back online (passing a health check).


[Coding Challenges](https://codingchallenges.fyi/challenges/challenge-load-balancer)

## Step 1

Create a basic server that can start-up, listen for incoming connections and then forward them 
to a single server.

The first sub-step then is to create a program (I'll call it `lb`) that will start up and listen
for connections on a specified port (i.e. 80 for HTTP). I’d suggest you then log a message to 
standard out confirming an incoming connection, something like this:

```
./lb
Received request from 127.0.0.1
GET / HTTP/1.1
Host: localhost
User-Agent: curl/7.85.0
Accept: */*
```