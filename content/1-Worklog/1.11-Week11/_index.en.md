---
title: "Worklog Week 11"
date: 2026-07-13
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Build Lambda functions for the game system maintenance mode.
* Separate functionality into independent Lambdas: Start Maintenance, Stop Maintenance, Vacuum & Analyze, Reset Daily.
* Configure EventBridge to automatically trigger Lambdas on schedule or by events.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Mon | - Design maintenance system architecture:<br>+ Identify required maintenance modes.<br>+ Design system state transition flow (online -> maintenance -> online).<br>+ Define API locking mechanism during maintenance. | 14/07/2026 | 14/07/2026 | |
| Tue | - Build Start Maintenance & Stop Maintenance Lambdas:<br>+ Start Maintenance: update API Gateway stageVariables, block new requests, notify maintenance.<br>+ Stop Maintenance: restore stageVariables, allow requests again.<br>+ Integrate with API Gateway SDK for state changes. | 15/07/2026 | 15/07/2026 | |
| Wed | - Build Vacuum & Analyze Lambda:<br>+ Automatically run VACUUM to clean up dead tuples in the database.<br>+ Run ANALYZE to update query planner statistics.<br>+ Log results and send completion notification. | 16/07/2026 | 16/07/2026 | |
| Thu | - Build Reset Daily Lambda:<br>+ Handle daily data reset (quests, daily gifts, free plays...).<br>+ Ensure data consistency during reset.<br>+ Log and notify reset results. | 17/07/2026 | 17/07/2026 | |
| Fri - Sat | - Configure EventBridge and test:<br>+ Create EventBridge rules for each Lambda with specific schedules.<br>+ Set up CloudWatch Metrics and logs for maintenance tasks.<br>+ Test the complete automated maintenance flow. | 18/07/2026 | 19/07/2026 | |

### Week 11 Results:

* Completed maintenance system architecture design with clear operation modes.
* Successfully built Start Maintenance and Stop Maintenance Lambdas, enabling flexible system state transitions via API Gateway stageVariables.
* Vacuum & Analyze Lambda operates effectively, automatically cleaning the database and optimizing query planner periodically.
* Reset Daily Lambda ensures daily data is reset correctly and consistently.
* Configured EventBridge rules to automatically trigger Lambdas on schedule:
  * Vacuum & Analyze: runs daily at 2:00 AM.
  * Reset Daily: runs daily at 0:00 AM.
  * Maintenance: triggered manually or automatically when needed.
* Automated maintenance system minimizes downtime and increases system stability.
