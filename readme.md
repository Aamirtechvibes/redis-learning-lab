# Redis TTL

## What I learned

TTL defines how long a Redis key remains available
before Redis automatically removes it.

## Experiment

SET product:101 "iPhone"
EXPIRE product:101 30

Then check:

TTL product:101

## Why it matters

TTL is one of the core mechanisms I'll use later
for dynamically controlling e-commerce product cache lifetime.