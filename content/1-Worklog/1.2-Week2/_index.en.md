---
title: "Worklog Week 2"
date: 2026-05-11
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Explore AWS services such as EC2, RDS, Route 53, S3 to find the optimal services for the Backend Game API project.
* Survey and design the overall architecture solution for the project.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources |
| --- | --- | --- | --- | --- |
| Tue | - Learn Amazon EC2: instance types, AMI, EBS, Elastic IP, Security Groups. <br> - Learn Amazon RDS: database engines (MySQL, PostgreSQL, Aurora), instance classes. | 12/05/2026 | 12/05/2026 | |
| Wed | - Learn Amazon Route 53: DNS management, routing policies, hosted zones. <br> - Learn Amazon S3: bucket, object storage, use cases for games (asset storage, backup). | 13/05/2026 | 13/05/2026 | |
| Thu - Fri | - Compare and evaluate AWS services suitable for the Backend Game API project. <br> - Determine the optimal architecture: combine EC2 for compute, RDS for database, S3 for asset storage. | 14/05/2026 | 15/05/2026 | |
| Sat - Sun | - Design the overall architecture solution for the project. <br> - Draw preliminary architecture diagram: <br> &emsp; + Client -> EC2 (Game Server) -> RDS (Database). <br> &emsp; + S3 for static asset storage. <br> &emsp; + Route 53 for domain management. <br> - Present and discuss the solution with the team. | 16/05/2026 | 17/05/2026 | |

### Week 2 Results:

* Mastered core AWS services: EC2, RDS, Route 53, S3 and how they apply to the Backend Game API project.
* Evaluated and selected optimal services based on technical requirements and cost considerations.
* Completed the solution survey and designed a preliminary architecture diagram for the system.
* Identified the main data flow: Client request -> EC2 (game logic processing) -> RDS (data storage), with static assets served from S3.
