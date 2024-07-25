
## Computer Architecture
- understand only binary, bit(0 or 1), 1 byte - 8bits(A,1)
- Disk storage(HDD, SDD), non volatile
- RAM, volatile (stores DS, variables and application data currently in use)
- Cache (fastest) - L1, L@, L3 then RAM
- CPU, processes operation defined in program.
- compiler converts high level code to machine code.

## Production App Architecture
- CI/CD (Code goes directly to production through some tests without manual intervention) Jenkins, github actions.
- Load Balancers (Nginx)
- Storage Server
- Logging and Monitoring servers (PM2(BE), sentry(FE))
- Alert Service
- Staging Environment
- Difficult to refactor at later stages therefore needs time to be thought through.

## Design Requirements
- Scalability, Maintainability, Efficiency, Reliability
- Moving data, Storing Data(access, indexing, backup), Transforming Data

### CAP/ Brewer's Theorem
- Consistency, Availability, Partition Tolerance
- can be achieved 2 out of three
- Banking System(CP)  
- uptime (SLO - Service Level Objectives), downtime(SLA - Service Level Agreements)
- Reliability, Fault Tolerance, Redundancy
- Speed (Throughput, Latency)
- Throughput
    - Server throughput - RPS
    - DB throughput - QPS
    - Data throughput -B/s
- Latency - single Request takes how much time
 
## Networking
- IP Address(IPv4 32 bit, IPv6 128bit)
- Internet Protocol(IP Header)
- Application Layer (http)
- Transport Layer (TCP (Reliability, delivery of complete package, 3 way handshake), UDP(faster, video calls, live streaming))
- DNS (maps ip address to website name)
- 

## Application Layer Protocol
- http (TCP/IP) ()
- Websockets (single long lived connection, all application that need real time data)
- SMTP (mails)
- FTP
- SSH
- WebRTC (Real time communication)
- MQTT
- AMQP
- RPC

## API Design
- CRUD
- POST /api/products
- GET  /api/products
- PUT  /api/products/:id
- DELETE /api/products/:id

- REST (over or under fetching), GraphQL, gRPC
- /api/users/:userId/orders
- /api/products?limit=100&offset=0
- /api/products?startDat={date}&endDate={date}
- Backward Compatibility and Versioning
- Rate Limiter
- CORS settings

## Caching and CDN's 
- Caching(browser(Cache-Control), server, database, ) Cache Hit, Cache Miss(X-Cache)
- Write around cache, write-through cache, write-back cache
- Eviction Policies(LRU, FIFO, LFU)
- CDN (static content)
- pull-based and push-based
- Reduced latency, high availability, improved security
  
## Proxy servers
- Intermediate server(caching, anonymous request, load balancing)
- Forward Proxy (Intercept request from client) control internet access (C -> FP -> S) (Caching, Anonymity)
- Reverse Proxy (Intercept request from internet) (Load Balancers, CDN, Firewalls(WAFs), SSL offloading)
- Open proxy
- Transparent Proxy
- Anonymous Proxy
- Distorting Proxy
- High Anonymity Proxy (does not contain x-forwarded value in header)

## Load Balancers
- distribute incoming traffic to different servers
- Round Robin
- Least Connection
- LRT (Least Response Time)
- IP Hash(session persistence)
- Weighted Algorithms
- Geographic
- Consistent Hashing
- Health checks
- hardware load balancer - f5, citrix
- software load balancer - HAPROXY, NGINX
- Failover strategy - Redundancy, Auto scailing and self healing, health checks, DNS Failover

## Databases
- Relational MySQL, SQLite - Tables, SQL (ACID)
- ACID(Atomicity, Consistency, Isolation, Durability)
- NoSQL Mongodb, neo4j (C is dropped for ACID)
- InMemory DB(Reddis, MemCache)
- Vertical Scaling(Incresing resources on single machine)
- Horizontal Scailing(Increasing machines)
    - Data Sharding (Spliting data into mutliple machines)
    - Data replication (Master - Slave)
- Caching, Indexing, Query Optimization
- (CAP Theorem)

