# Domain Name System (DNS)

## What is DNS?
- **DNS** is a **hierarchical, distributed naming system** that maps **domain names** to **IP addresses** .
- It allows users to access websites using human-readable names instead of numeric IPs.

---

## How DNS Works
1. **User Input**: A user types a domain name in the browser.
2. **Local Cache Check**: The browser checks if the IP is cached.
3. **DNS Resolver Query**: Sent to a resolver (usually ISP).
4. **Root DNS Server**: Points to the TLD server.
5. **TLD Server**: Points to the authoritative DNS server.
6. **Authoritative Server**: Returns the actual IP address.
7. **Final Response**: The browser connects to the correct server.

---

## DNS Hierarchical Structure
- **Root DNS Servers**: Top-level, direct queries to TLD servers.
- **TLD Servers**: Handle extensions like `.com`, `.org`, etc.
- **Authoritative Servers**: Contain actual domain records (A, MX, etc.).

---

## Types of Domains
- **Generic**: .com, .org, .net
- **Country Code**: .in, .us, .uk
- **Inverse Domains**: Used for reverse DNS lookups

---

## DNS Lookup (Resolution)
- Converts domain names into IP addresses.
- Sequence: Resolver → Root → TLD → Authoritative → Response

---

## DNS Resolver
- Also called **DNS client**.
- Initiates DNS resolution on behalf of applications.

---

## Types of DNS Queries
1. **Recursive**: Resolver returns final answer or error.
2. **Iterative**: Resolver returns best info it has.
3. **Non-Recursive**: Resolver already has the answer cached.

---

## DNS Caching & TTL
- **Caching** improves speed and reduces traffic.
- **TTL (Time-to-Live)** defines how long DNS info is stored locally before requiring refresh.

---

## Common DNS Record Types
| Record | Purpose |
|--------|---------|
| **A**       | Maps domain to IPv4 address |
| **CNAME**   | Aliases one domain to another |
| **MX**      | Specifies mail server for domain |
| **TXT**     | Stores text data (e.g., SPF, DKIM) |

---
