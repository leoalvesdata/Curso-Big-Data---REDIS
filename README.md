# Redis Data Management Project

## Description
[cite_start]This project demonstrates the use of **Redis (NoSQL)** to manage user sessions, interests, and visit counts[cite: 33, 47]. It simulates real-time data handling for a web platform scenario.

## Technical Implementation

### User State & Counters
* [cite_start]**`SET`**: Used for current session data, including the last visit, date, and interests[cite: 4, 7, 8].
* [cite_start]**`INCR`**: Implemented for atomic increments of visit counters to ensure data consistency[cite: 24].
* [cite_start]**`EXPIRE`**: Used to manage session timeouts (set to 30 seconds), simulating security and memory management[cite: 34, 38].

### Historical Data Tracking
* [cite_start]**Lists (`RPUSH`)**: Chosen for "Interest History" to preserve the chronological order of visited pages, following a FIFO (First-In, First-Out) logic[cite: 19, 20].
* [cite_start]**Sorted Sets (`ZADD`)**: Used for "Access Dates"[cite: 21]. [cite_start]I utilized a numeric score in the `YYYYMMDD` format to ensure the Redis engine automatically orders visits from the oldest to the newest[cite: 21, 29].

### Data Operations
* [cite_start]**Sorting**: Used the `SORT ... ALPHA` command to organize text-based interests alphabetically for better visualization[cite: 43, 44, 46].
* [cite_start]**Set Union**: Demonstrated the use of `SADD` and `SUNIONSTORE` to aggregate unique user names from different sets into a single new variable[cite: 47, 48, 49, 55].

---
## About Me
I am a **PhD candidate in Agronomic and Forestry Sciences**, currently expanding my expertise into **Big Data** to bridge the gap between **Environmental Sciences and Data Engineering**. This project represents my initial steps into the world of NoSQL databases and high-performance data structures.
