---
layout: post
title: "CAP Theorem, ACID vs BASE"
date: 2026-04-06
categories: [Databases]
---

In my last post, I did state that in my next post I would discuss the architecture to take my Policy Admin System from a Static Web App to production, but then it hit me, would my readers understand what I mean if I start discussing CAP Theorem, ACID, BASE, back-pressure, design patterns for Azure Functions, persimistic vs optimistic... probably not. So let's start with CAP Theorem and ACID vs BASE.

Modern distributed systems force us to make trade-offs that traditional single-node databases largely hid from us. Among the most important conceptual tools for understanding these trade-offs are the CAP Theorem and the contrasting philosophies of ACID and BASE. This post walks through these ideas and argues for a pragmatic hybrid approach that reflects how real-world systems are built today.

---

## The CAP Theorem (Consistency, Availability, Partition Tolerance)

The CAP Theorem states that in a distributed data system, you can only guarantee two out of three of the following properties:

- Consistency (C)
  Every read receives the most recent write (or an error).

- Availability (A)
  Every request receives a response, even if it’s not the latest data.

- Partition Tolerance (P)
  The system continues to operate despite network partitions (communication breakdowns between nodes).

### The Practical Reality

In distributed systems, partition tolerance is non-negotiable because networks will fail. That means the real trade-off is Consistency vs Availability

This leads to two dominant system types:

- CP systems: Prioritize consistency over availability
  (e.g., reject requests if consistency cannot be guaranteed)

- AP systems: Prioritize availability over consistency
  (e.g., serve potentially stale data but remain responsive)

---

## ACID: Strong Guarantees for Reliable Transactions

ACID is the traditional model used by relational databases:
- Atomicity – All or nothing execution
- Consistency – Valid state transitions only
- Isolation – Concurrent transactions don’t interfere
- Durability – Committed data is permanent

It's strengths include predictable behavior, strong data integrity and easier reasoning about correctness. But it's limitations are high coordination cost (e.g., two-phase commit), reduced availability under partition and latency overhead.

ACID systems map closely to **CP** in the CAP space.

---

## BASE: Embracing Availability and Scale

BASE emerged from large-scale distributed systems:

- Basically Available – System remains responsive
- Soft state – State may change over time
- Eventually consistent – Consistency is achieved later

It's strengths include High Availability, better horizontal scalability and lower latency. But it's limitations include temporary inconsistency, increased application complexity and harder correctness guarantees.

BASE systems align with **AP** in CAP.

---

## The Hybrid Approach: Best of Both Worlds

Modern architectures rarely commit fully to either extreme. Instead, they combine strategies based on workload requirements. When designing a system, ask:

- What data must never be inconsistent?
- What latency is acceptable?
- What happens during network failure?
- Can the application tolerate stale reads?

| Requirement              | Prefer    |
| ------------------------ | --------- |
| Financial correctness    | ACID / CP |
| User experience (uptime) | BASE / AP |
| Large-scale reads        | BASE      |
| Critical state mutation  | ACID      |

---

## Final Thoughts

CAP doesn’t give you a choice—it gives you a constraint. Once you accept that network partitions are inevitable, every system design becomes a decision about where you sit between consistency and availability.

ACID and BASE aren’t opposing camps so much as tools. ACID gives you correctness and guarantees; BASE gives you resilience and scale. The challenge is knowing where each matters.

In practice, strong consistency is reserved for critical operations like financial transactions or state changes, while eventual consistency is used to keep systems responsive and scalable under load.

The goal isn’t to pick a side, it’s to design boundaries. Get those right, and you end up with a system that behaves correctly where it must, and remains available where it should.


