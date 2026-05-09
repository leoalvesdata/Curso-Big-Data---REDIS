# Curso-Big-Data---REDIS

Description
This project demonstrates the use of Redis (NoSQL) to manage user sessions, interests, and visit counts.

Technical Implementation
1. User State & Counters
Used SET for current session data (last visit, date, interests).
Implemented INCR for atomic increments of visit counters.
Used EXPIRE to manage session timeouts (simulating security/memory management).

2. Historical Data Tracking
Lists (RPUSH): Chosen for "Interest History" to preserve the chronological order of visited pages (FIFO logic).
Sorted Sets (ZADD): Used for "Access Dates". I used a numeric score (YYYYMMDD) to ensure the Redis engine automatically orders visits from oldest to newest.

3. Data Operations
Sorting: Used SORT ... ALPHA to organize text-based interests alphabetically.
Set Union: Demonstrated the use of SADD and SUNIONSTORE to aggregate unique users from different sets into a new variable.

I am a PhD candidate in Agronomic and Forestry Sciences, currently expanding my expertise into Big Data and Data Engineering field to bridge the gap between Environmental Sciences and Data Engineering.
