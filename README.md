# Low_High_System_Designs

- Some low and high level system design notes
- [SD Components](https://interviewready.io/blog/system-design-component-examples)
- [Gaurav Sen paid course](https://interviewready.io/course-page/system-design-course)

## CDN(Content Delivery Networks)

- faster and cheaper
- caching, DS(Distributed System)
- static data(videos, images, files)

### Problems with server serving html pages
- The server cannot be at all regions which might slow down the speed with which html pages are rendered depending on location   
- Some content has to be served locally according to specific region(some movies might be banned in some regions). 
### Solution
- CDN - we can move cache to specific locations, this cache is actually a server. All these small servers have a mother server.
- close to user
- follow regulations
- content update from server
- e.g, Amaazon CloudFront(Integration with amazon S3) - cheap, reliable, easy to use.


## Distributed Systems

### Caching - user to server(similar user we store it in local memory and return the data)
#### Cache Policy (LRU, LFU)
- Poor hit rate of cache effect the query time.(Thrashing- increases latency)
- Eventual Consistency - when to update the cache with the latest value from database.
- Cache placement
### Load Balancer - Scaling Horizontally with several servers rather than a single powerful computer(Horizontal Scaling)
#### Algos
  - Round-Robin (1 by 1 to all the servers)
  - Geo-based (depending on regions)
  - Least Connections (state is managed, routes to least number of connection)
  - Hybrid(like geo used for the server than round robin for the service)

## Low Level System Design Patterns

### Creational Design Pattern

#### Factory Method 

#### Abstract Factory Method

#### Singleton Method

#### Prototype Method

#### Builder Method

### Structural Design Pattern

#### Adapter Method

#### Bridge Method

#### Composite Method

#### Decorator Method

#### Facade Method

#### Flyweight Method


#### Proxy Method


### Behavioural Design Pattern

#### Chain of Responsibility Method

#### Command Method

#### Interpreter Method


#### Mediator Method

#### Memento Method

#### Observer Method

#### State Method

#### Strategy Method


#### Template Method


#### Visitor Method
