# SimpleYelp — Local Lifestyle Notes Platform

A review service where users post dining/exploration notes. Implemented user login, ordering, coupon
flash sales, note publishing, and article like/bookmark features.

## Architecture (High Level)
```
Client ──> Nginx ──> Spring Boot (Auth / Notes / Orders / Coupons / Feed)
                         │
        MySQL <──────────┼──────────> Redis (cache, session, locks, stock)
                         │
                      Kafka <────── Kafka Streams (hot-note ranking)
```

### Prerequisites
- JDK 17+ and Maven/Gradle  
- **MySQL** and **Redis** running locally or via Docker  
- **Kafka + Zookeeper** (for message queue & Streams)  
- **Nginx** for reverse proxy/load balancing

## License
MIT License © 2025 zifeiyuu

