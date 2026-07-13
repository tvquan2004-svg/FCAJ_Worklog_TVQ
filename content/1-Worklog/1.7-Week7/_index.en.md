---
title: "Worklog Week 7"
date: 2026-06-15
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Develop Dependent Services for game logic: Shop, Gift Code.
* Build Cross-Service Communication mechanism via API Gateway for Lambda functions to interact with each other.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Mon | - Design architecture for lambda-transaction:<br>+ Identify required API endpoints.<br>+ Plan data flow between lambda-transaction and core services (lambda-economy, lambda-inventory). | 16/06/2026 | 16/06/2026 | |
| Tue | - Develop Shop functionality:<br>+ Build API for purchasing items with Coin/Gem.<br>+ Implement balance checking and deduction logic.<br>+ Update player inventory after transactions. | 17/06/2026 | 17/06/2026 | |
| Wed | - Develop Gift Code functionality:<br>+ Build API for creating and redeeming Gift Codes.<br>+ Implement code validation, expiry checking, and usage limit.<br>+ Handle item/resource reward distribution. | 18/06/2026 | 18/06/2026 | |
| Thu - Fri | - Build Cross-Service Communication:<br>+ Set up API Gateway as communication intermediary between Lambdas.<br>+ Configure IAM Role for cross-Lambda invocation.<br>+ Handle errors and timeouts in inter-service communication. | 19/06/2026 | 20/06/2026 | |
| Sun | - Integration testing of the full transaction flow:<br>+ Buy item from Shop -> deduct currency -> receive item.<br>+ Redeem Gift Code -> validate code -> distribute reward.<br>+ Verify data consistency across services. | 21/06/2026 | 21/06/2026 | |

### Week 7 Results:

* Completed design and development of lambda-transaction with all required API endpoints for Shop and Gift Code.
* Shop system operates stably: players can purchase items, the system automatically checks balances, deducts currency, and updates inventory accurately.
* Gift Code functionality successfully deployed with code validation, expiry checking, and usage limit mechanisms.
* Successfully built Cross-Service Communication via API Gateway, enabling Lambda functions to communicate safely and efficiently.
* Completed integration testing, ensuring data consistency across all transaction flows.
