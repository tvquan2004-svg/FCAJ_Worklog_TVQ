---
title: "Worklog Week 5"
date: 2026-06-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Set up Monorepo with npm Workspaces for multi-service source code management.
* Build a standard Lambda Handler Pattern for all services.
* Configure Serverless Framework for each service to deploy to AWS.
* Connect to the database using TypeORM with IAM Auth.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Tue | - Set up Monorepo with npm Workspaces: <br> + Directory structure: packages/shared, services/*. <br> + Initialize root package.json with workspaces. <br> + Share common code (types, utils) via shared package. | 02/06/2026 | 02/06/2026 | |
| Wed | - Build Lambda Handler Pattern: <br> + Design base handler class with error handling, logging, response format. <br> + Middleware pattern: authentication, validation, rate limiting. <br> + Standard response format for all API endpoints. | 03/06/2026 | 03/06/2026 | |
| Thu | - Configure Serverless Framework: <br> + Create serverless.yml for each service. <br> + Configure provider: runtime, region, stage, IAM Role. <br> + Configure functions, events, environment variables. <br> + Plugins: serverless-offline, serverless-dotenv. | 04/06/2026 | 04/06/2026 | |
| Fri | - Connect database via TypeORM + IAM Auth: <br> + Configure TypeORM DataSource with Aurora PostgreSQL. <br> + Integrate IAM Auth: use AWS SDK to get database auth token. <br> + Create entities and migrations for data tables. | 05/06/2026 | 05/06/2026 | |
| Sat - Sun | - Integration testing: <br> + Build monorepo, verify dependencies resolve correctly. <br> + Run Lambda handler locally with serverless-offline. <br> + Test database connection with IAM Auth. | 06/06/2026 | 07/06/2026 | |

### Week 5 Results:

* Successfully set up Monorepo with npm Workspaces, sharing common code via shared package for consistent source management across services.
* Built a standard Lambda Handler Pattern with base handler, middleware support, and unified response format.
* Configured Serverless Framework completely for each service with full functions, events, and environment variables.
* Connected to the database successfully using TypeORM + IAM Auth, using database auth tokens instead of traditional passwords for enhanced security.
* Created entities and migrations for core data tables, ready for business logic development.
