# Redis Learning Lab ⚡

A hands-on journey into **Redis, caching, TTLs, and backend performance**.

I'm learning Redis by building small, practical experiments instead of just watching tutorials — and gradually applying what I learn to real-world backend problems.

## 🧠 Learning Path

* [x] Redis fundamentals
* [x] Local Redis setup with Docker
* [x] Redis with Node.js
* [x] Basic Redis commands — `GET`, `SET`, `DEL`
* [x] TTL & key expiration
* [x] Temporary data with Redis — OTP
* [x] Basic caching — Banner Cache
* [ ] Redis data types
* [ ] Cache-aside pattern
* [ ] Cache hit / miss analysis
* [ ] LRU & LFU eviction
* [ ] Cache invalidation
* [ ] Cache stampede
* [ ] Hot keys
* [ ] Rate limiting
* [ ] Pub/Sub
* [ ] Dynamic TTL
* [ ] Redis performance benchmarking
* [ ] Intelligent caching

---

## 🛠️ Projects

### 01 — Banner Cache

A small Redis caching experiment for serving frequently requested banner data without repeatedly querying the database.

**What I learned:**

* Redis caching
* Cache hit / miss
* `GET` / `SET`
* Reducing unnecessary database reads
* Using Redis for frequently accessed data

---

### 02 — OTP Verification

A short-lived OTP verification system built with **Node.js + Express + Redis**.

```text
Generate OTP
     ↓
Redis SET
     ↓
TTL = 30 seconds
     ↓
Redis GET
     ↓
Verify
     ↓
Redis DEL
```

**What I learned:**

* TTL-based expiration
* Temporary data storage
* `SET ... EX`
* `GET`
* `TTL`
* `DEL`
* Automatic expiration without manual cleanup

---

## 🎯 Why I'm Learning Redis

I'm interested in Redis because caching isn't just about making an API "faster".

It's about deciding:

> **What data should live in memory, for how long, and when should it disappear?**

Redis can help reduce unnecessary database reads, improve response times, handle frequently accessed data, and keep short-lived application state out of the primary database.

---

## 🚀 Real-World Goal

After completing the Redis fundamentals, I'll apply what I've learned to **Coffee on QR**, my hospitality-tech startup.

The goal is to build an intelligent caching layer for things like:

* Event banners & popups
* Frequently accessed public data
* Cafe/menu data
* Popular content

Eventually, I want to experiment with **dynamic TTLs based on traffic and popularity** rather than relying on fixed caching rules.

```text
User Request
      ↓
   Redis
   ↙   ↘
 HIT    MISS
  ↓       ↓
Return  Database
          ↓
        Redis
          ↓
        Return
```

---

## 📈 End Goal

Build a practical understanding of Redis and eventually turn it into an **intelligent caching system** that can measure:

* Cache Hit Rate
* Cache Miss Rate
* Database Requests
* Response Latency
* Memory Usage
* Cost Savings

---

### Learning by building > Learning by watching.

More experiments coming. 🚀