---
title: "Worklog Week 6"
date: 2026-06-08
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Build Core Services for the Backend Game API system.
* Develop lambda-auth: user authentication and authorization.
* Develop lambda-inventory: inventory and equipment management.
* Develop lambda-economy: in-game currency management (Coin, Gem).

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Tue | - Detail design of Core Services: <br> + Define API endpoints for each service. <br> + Design database schema: users, inventory_items, currencies. <br> + Define data flow between services. | 09/06/2026 | 09/06/2026 | |
| Wed | - Develop lambda-auth: <br> + Build signup, sign-in, refresh token APIs. <br> + JWT token validation. <br> + Authentication middleware for other services. | 10/06/2026 | 10/06/2026 | |
| Thu | - Develop lambda-inventory: <br> + API to add items to inventory. <br> + API to list items, equipment. <br> + API to equip/unequip items. <br> + Update item quantities on usage. | 11/06/2026 | 11/06/2026 | |
| Fri | - Develop lambda-economy: <br> + API to add/deduct Coin, Gem. <br> + API to check balance. <br> + API for transaction history. <br> + Handle concurrent transactions safely. | 12/06/2026 | 12/06/2026 | |
| Sat - Sun | - Test Core Services: <br> + Test each Lambda individually. <br> + Test integration flow: auth -> inventory/economy. <br> + Verify error handling. <br> + Optimize Lambda performance. | 13/06/2026 | 14/06/2026 | |

### Week 6 Results:

* Completed detailed design of Core Services architecture with full API endpoints and database schema.
* lambda-auth fully developed: sign-up, sign-in, JWT authentication, refresh token, auth middleware.
* lambda-inventory operational with full functionality: inventory management, add/remove items, equip/unequip.
* lambda-economy manages in-game currency (Coin, Gem) with safe concurrent transaction handling and detailed transaction history.
* Integration testing successful: authentication -> authorization -> business logic flow works stably.
* All 3 Core Services ready for deployment, serving as the foundation for Dependent Services in the following weeks.
