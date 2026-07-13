---
title: "Worklog Week 8"
date: 2026-06-22
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Create a centralized HTTP API V2 to manage all system endpoints.
* Configure routing for each service and deploy to AWS.
* Test all system APIs.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Mon | - Design HTTP API V2 structure:<br>+ Identify routes for each service (auth, inventory, economy, transaction).<br>+ Plan mapping between API Gateway paths and Lambda functions. | 23/06/2026 | 23/06/2026 | |
| Tue | - Create HTTP API V2 on API Gateway:<br>+ Configure CORS for client access.<br>+ Set up stages (dev, staging, prod).<br>+ Integrate Lambda authorizer for authenticated endpoints. | 24/06/2026 | 24/06/2026 | |
| Wed | - Configure detailed routing:<br>+ Define routes and integrations for each Lambda.<br>+ Set up request/response transformation if needed.<br>+ Configure throttle and rate limiting. | 25/06/2026 | 25/06/2026 | |
| Thu | - Deploy all Compute Services + API Gateway:<br>+ Deploy Lambda functions to AWS.<br>+ Update environment variables and permissions.<br>+ Deploy API Gateway to production stage. | 26/06/2026 | 26/06/2026 | |
| Fri - Sat | - Comprehensive API system testing:<br>+ Test each endpoint individually.<br>+ Test end-to-end flows.<br>+ Verify error handling and response codes.<br>+ Optimize performance (cold start, latency). | 27/06/2026 | 28/06/2026 | |

### Week 8 Results:

* Successfully designed and deployed a centralized HTTP API V2 managing all routes for all services.
* Completed detailed routing configuration with CORS, Lambda authorizer, and stage environments.
* Successfully deployed all Compute Services (lambda-auth, lambda-inventory, lambda-economy, lambda-transaction) to AWS.
* API Gateway deployed to production stage and ready to serve.
* Completed comprehensive testing:
  * All endpoints function correctly.
  * End-to-end flow: authentication -> authorization -> business logic -> response works stably.
  * Error handling returns appropriate status codes (400, 401, 403, 404, 500).
  * Cold start optimized by increasing Lambda allocated memory.
