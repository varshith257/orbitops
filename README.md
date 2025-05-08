# 🚀 OrbitOps

### Scheduling • Observability • Multi-Agent Coordination

**OrbitOps** is an open-source platform designed to revolutionize how scheduling systems, system observability and multi-agent coordination come together.

We orbit around three pillars:
✅ Powerful scheduling backend  
✅ Robust observability + health monitoring  
✅ Experimental multi-agent workflows using Model Context Protocol (MCP)

---

## ✨ Key Features

🌐 Next.js + Tailwind frontend  
🔗 tRPC API + Prisma backend  
🛢️ Postgres database  
🛡️ Sentry, Checkly
🤖 Experimental MCP agent layer (rescheduler, optimizer, negotiator)  
🐳 Dockerized, production-ready deployment

---

## ⚙️ Architecture Overview

```text
+-------------------------------+
|         Frontend Layer        |
|   - Next.js                  |
|   - Tailwind UI              |
|   - User Booking Dashboard   |
+--------------+----------------+
               |
               | (tRPC API calls)
               v
+-------------------------------+
|         Backend Layer         |
|   - Node.js                  |
|   - tRPC Router              |
|   - Scheduling Logic         |
|   - User/Slot/Booking CRUD   |
|   - MCP Agent Integration    |
+--------------+----------------+
               |
               | (Database queries via Prisma)
               v
+-------------------------------+
|        Database Layer         |
|   - Postgres (or SQLite)     |
|   - Prisma ORM Models        |
|   - Stores users, slots,     |
|     bookings, agent logs     |
+--------------+----------------+
               |
               | (System logs, events, metrics)
               v
+-------------------------------+
|      Observability Layer      |
|   - Sentry (errors)          |
|   - Axiom/Checkly (metrics) |
|   - Grafana (optional)       |
+--------------+----------------+
               |
               | (Agent signal triggers, MCP messages)
               v
+-------------------------------+
|   MCP Coordination Layer      |
|   - Agent A (rescheduler)    |
|   - Agent B (conflict check)|
|   - Agent C (notifications) |
|   - JSON-based MCP protocol  |
|   - Negotiates + automates  |
+-------------------------------+
