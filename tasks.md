## 🗂️ Obsidian Folder Structure (Recommended)

```
/Project-Monorepo/
├── 00-Roadmap.md
├── 01-Epics/
│   ├── User-Service.md
│   ├── Product-Service.md
│   ├── Vendor-Portal.md
│   └── Frontend-System.md
├── 02-Tasks/
│   ├── TASK-001-JWT-Auth.md
│   ├── TASK-002-Kafka-Order-Events.md
│   └── ...
├── 03-Backlog.md
├── 04-Completed.md
```

---

## 📋 Kanban Table Template (Markdown)

```markdown
## 🏗️ Project Kanban Board

| Status         | Task ID  | Title                            | Epic            | Priority | Notes                 |
| -------------- | -------- | -------------------------------- | --------------- | -------- | --------------------- |
| ✅ Done        | TASK-001 | Setup base Git repo for monorepo | Project Setup   | High     |                       |
| 🟡 In Progress | TASK-014 | Implement JWT Authentication     | User Service    | High     |                       |
| 🔲 To Do       | TASK-022 | Add multi-product image uploads  | Product Service | Medium   |                       |
| ⏸️ Blocked     | TASK-037 | Video calls with Pion WebRTC     | WebRTC Service  | High     | Waiting for ICE setup |
```

---

## 🧱 50 Detailed Task Ideas (Grouped by Epic)

---

### 📦 **EPIC: Project Setup & Architecture**

- TASK-001: Setup base Git repositories (frontend, backend, proto)
- TASK-002: Define architecture diagram (draw\.io or Excalidraw)
- TASK-003: Configure `buf` for protobuf repo
- TASK-004: Setup Docker & Docker Compose for local dev
- TASK-005: Create README & CONTRIBUTING guidelines
- TASK-006: Configure GitHub Actions for CI
- TASK-007: Set up centralized logging with Loki
- TASK-008: Create Helm charts for Kubernetes deployment

---

### 🔐 **EPIC: User Service**

- TASK-009: Implement registration & login with email/password
- TASK-010: Add Google OAuth2 login
- TASK-011: Implement JWT access + refresh token handling
- TASK-012: Add multi-factor authentication (TOTP)
- TASK-013: Role & permission system (RBAC)
- TASK-014: Add session management (device tracking)
- TASK-015: Upload profile pictures with resumable uploads

---

### 🛍️ **EPIC: Product Catalog Service**

- TASK-016: Add product creation/editing flow
- TASK-017: Create draft → publish flow
- TASK-018: Setup product tagging + autocomplete
- TASK-019: Support multi-image upload w/ preview
- TASK-020: Add bulk CSV product import
- TASK-021: Generate SEO-friendly slugs and metadata
- TASK-022: Add soft-delete & audit logging

---

### 🛒 **EPIC: Order Service**

- TASK-023: Implement shopping cart management
- TASK-024: Create checkout flow with address validation
- TASK-025: Order placement with Saga coordination
- TASK-026: Support cancel/refund workflows
- TASK-027: Add order invoice PDF generation
- TASK-028: Log Kafka `order-events` topic

---

### 💳 **EPIC: Payment Service**

- TASK-029: Integrate Stripe and test sandbox payments
- TASK-030: Add internal transaction ledger
- TASK-031: Implement retry-safe webhook handling
- TASK-032: Set up subscription billing logic
- TASK-033: Create invoice viewer UI (React or Nuxt)
- TASK-034: Add fraud detection rule system

---

### 🏪 **EPIC: Vendor Dashboard**

- TASK-035: Create vendor registration and KYC upload
- TASK-036: Build storefront customization tools
- TASK-037: Add vendor analytics dashboard
- TASK-038: Integrate wallet and payout system
- TASK-039: Handle buyer disputes (moderation tool)

---

### 💬 **EPIC: Chat & Real-Time**

- TASK-040: Setup Centrifugo WebSocket bridge
- TASK-041: Build chat UI with typing indicators
- TASK-042: Implement message persistence in PostgreSQL
- TASK-043: Add push notification fallback
- TASK-044: Setup chat moderation API

---

### 📹 **EPIC: WebRTC Service**

- TASK-045: Setup STUN/TURN config for Pion
- TASK-046: Add screen-sharing support
- TASK-047: Log call metadata (who, when, how long)
- TASK-048: Implement call permission checks
- TASK-049: Add audio-only fallback

---

### 🚀 **EPIC: DevOps & Monitoring**

- TASK-050: Setup Prometheus + Grafana for metrics dashboard

---

## 🗂️ BONUS: Task File Format in Obsidian

You can create `.md` files per task inside `02-Tasks/`. Here's a sample:

```markdown
# TASK-014: Implement JWT Authentication

**Epic**: User Service  
**Status**: In Progress  
**Priority**: High  
**Assignee**: Me  
**Due Date**: 2025-05-30

## Description

Implement JWT-based login using access + refresh tokens. Store secret keys in Vault.
Ensure tokens are stateless and short-lived.

## Checklist

- [x] Generate JWT with user ID & roles
- [x] Create login endpoint
- [x] Add refresh token logic
- [ ] Unit tests for auth flow
- [ ] Integration test with API gateway

## Notes

Consider adding device-based session tracking next.
```
