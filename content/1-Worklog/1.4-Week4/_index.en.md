---
title: "Worklog Week 4"
date: 2026-05-25
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Create an Amazon Aurora PostgreSQL cluster as the primary database for the system.
* Configure RDS Proxy to pool connections and reduce database load during Lambda scaling.
* Create a CloudFormation Stack to automate infrastructure deployment.
* Update IAM Policy with actual cluster-id and database-user-name.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources |
| --- | --- | --- | --- | --- |
| Tue | - Learn about Amazon Aurora PostgreSQL: <br> + Cluster architecture, writer/reader instances. <br> + Compare Aurora with standard RDS MySQL/PostgreSQL. <br> + Configuration parameters: instance class, storage, backup. | 26/05/2026 | 26/05/2026 | |
| Wed | - Create Amazon Aurora PostgreSQL cluster: <br> + Configure VPC, subnet groups, security groups. <br> + Create writer instance for read/write operations. <br> + Set up automated backup and maintenance window. | 27/05/2026 | 27/05/2026 | |
| Thu | - Learn and configure RDS Proxy: <br> + How RDS Proxy pools connections from Lambda to reduce database load. <br> + Create RDS Proxy, connect to the Aurora cluster. <br> + Configure IAM Role for Lambda to use RDS Proxy. | 28/05/2026 | 28/05/2026 | |
| Fri | - Create CloudFormation Stack: <br> + Write CloudFormation template for the entire infrastructure. <br> + Create stack, deploy resources: Aurora, RDS Proxy, Security Groups. <br> - Update IAM Policy with actual cluster-id and database-user-name. | 29/05/2026 | 29/05/2026 | |
| Sat - Sun | - Test connection and finalize: <br> + Test connection from Lambda to Aurora via RDS Proxy. <br> + Verify IAM Auth works. <br> + Document configuration for the team. | 30/05/2026 | 31/05/2026 | |

### Week 4 Results:

* Successfully created an Amazon Aurora PostgreSQL cluster with writer instance, ready for production.
* Configured RDS Proxy successfully, pooling connections from Lambda and preventing connection exhaustion during sudden Lambda scaling.
* CloudFormation Stack deployed successfully, automating the entire Aurora + RDS Proxy infrastructure setup.
* IAM Policy updated with actual cluster-id and database-user-name, ensuring security and precise permission management.
* Lambda -> RDS Proxy -> Aurora connection tested and working stably.
