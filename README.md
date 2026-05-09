# Redis Data Management Project

## Description
This project demonstrates the use of **Redis (NoSQL)** to manage user sessions, interests, and visit counts. It simulates real-time data handling for a web platform scenario.

## Technical Implementation

### User State & Counters
*`SET`**: Used for current session data, including the last visit, date, and interests.
*`INCR`**: Implemented for atomic increments of visit counters to ensure data consistency.
*`EXPIRE`**: Used to manage session timeouts (set to 30 seconds), simulating security and memory management.

### Historical Data Tracking
*Lists (`RPUSH`)**: Chosen for "Interest History" to preserve the chronological order of visited pages, following a FIFO (First-In, First-Out) logic.
*Sorted Sets (`ZADD`)**: Used for "Access Dates". I utilized a numeric score in the `YYYYMMDD` format to ensure the Redis engine automatically orders visits from the oldest to the newest.

### Data Operations
*Sorting**: Used the `SORT ... ALPHA` command to organize text-based interests alphabetically for better visualization.
*Set Union**: Demonstrated the use of `SADD` and `SUNIONSTORE` to aggregate unique user names from different sets into a single new variable.

---
## About Me
I am a **PhD candidate in Agronomic and Forestry Sciences**, currently expanding my expertise into **Big Data** to bridge the gap between **Environmental Sciences and Data Engineering**. This project represents my initial steps into the world of NoSQL databases and high-performance data structures.
