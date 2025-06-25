# Load Balancer
A **Load Balancer** is a networking component (hardware or software) that distributes incoming network traffic across multiple servers to ensure:
- High availability
- Reliability
- Better performance
- Efficient resource utilization

## Why Load Balancer is Needed
Without a load balancer:
- A **single point of failure** can take down the entire app.
- Servers can become **overloaded**.
- **Scalability** becomes difficult.

## Key Characteristics
- **Traffic Distribution**
- **High Availability**
- **Horizontal Scalability**
- **Health Monitoring**
- **SSL Termination**
- **Resource Optimization**

## How Load Balancers Work
1. **Receive requests** from clients
2. **Monitor health** of servers
3. **Distribute traffic** based on algorithms or server status
4. **Redirect traffic** in case of server failure
5. **Improve performance**

---

## Types of Load Balancers
- **Hardware Load Balancer** – High performance, expensive
- **Software Load Balancer** – Cost-effective, flexible
- **Cloud Load Balancer** – Scalable, managed service
- **Layer 4** – Operates on transport layer (IP & Port)
- **Layer 7** – Operates on application layer (HTTP headers, URLs)
- **Global Server Load Balancer (GSLB)** – Routes based on geography

---

## Load Balancing Algorithms
### Static
- **Round Robin**
- **Weighted Round Robin**
- **Source IP Hash**

### Dynamic
- **Least Connections**
- **Least Response Time**

---

## Benefits
- Improved **performance**, **scalability**
- Better **fault tolerance**
- **Session persistence**
- **Traffic surge management**

## Challenges
- Can become a **single point of failure**
- **Complex setup** and **costly solutions**
- **SSL inspection** and configuration challenges

---

## Layer-4 vs Layer-7 Load Balancing

| Feature              | Layer-4                           | Layer-7                                 |
|----------------------|-----------------------------------|------------------------------------------|
| OSI Layer            | Transport Layer                   | Application Layer                        |
| Routing Criteria     | IP, Port, Protocol (TCP/UDP)      | Content, URL, Cookies, Headers           |
| Performance          | Faster                            | Slightly slower but smarter              |
| Cost                 | Lower                             | Higher                                   |
| Features             | Basic                             | Advanced (e.g., caching, session stickiness) |
| Best For             | High-speed traffic (DNS, Gaming)  | Web apps with complex routing needs      |

---

# Reverse Proxy

A **Reverse Proxy** is a server that sits between clients and backend servers, forwarding client requests and returning responses. It adds:
- **Security** (e.g., protection from DDoS)
- **Caching** (to reduce latency)
- **SSL Termination**
- **Performance enhancement**

---

## Reverse Proxy vs Load Balancer

| Feature              | Reverse Proxy                    | Load Balancer                             |
|----------------------|----------------------------------|--------------------------------------------|
| Purpose              | Security, performance, caching   | Distribute traffic across servers          |
| Caching              | Yes                              | Typically no                               |
| SSL Termination      | Yes                              | Yes                                        |
| Load Distribution    | May perform basic load balancing | Primary function                           |
| Best Use Case        | Web security & content delivery  | Scalability and fault tolerance            |
| Examples             | Nginx, Apache HTTP Server        | AWS ELB, HAProxy, F5 BIG-IP                |

---

## Conclusion
- **Load Balancer**: Focuses on distributing traffic and ensuring availability.
- **Reverse Proxy**: Acts as a secure and performance-enhancing gateway to backend servers.
- **Both** can be used together for enhanced **performance**, **security**, and **scalability** in modern system architectures.
