---
title: "Worklog Week 10"
date: 2026-07-06
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Build a Dead Letter Queue (DLQ) system to manage failed messages.
* Configure RedrivePolicy with maxReceiveCount to automatically move failed messages to DLQ.
* Set up CloudWatch Metrics and Alarms to monitor DLQ.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Mon | - Learn Dead Letter Queue architecture:<br>+ Role of DLQ in asynchronous processing systems.<br>+ How SQS integrates with DLQ to manage failed messages.<br>+ Configuration parameters: maxReceiveCount, retention period. | 07/07/2026 | 07/07/2026 | |
| Tue | - Configure RedrivePolicy:<br>+ Set maxReceiveCount = 3 (auto-move to DLQ after 3 failed retries).<br>+ Create dedicated DLQ queues per message type (game-economy-dlq.fifo, ...).<br>+ Configure 14-day message retention on DLQ. | 08/07/2026 | 08/07/2026 | |
| Wed | - Configure functionResponseType: ReportBatchItemFailures:<br>+ Allow Lambda to report individual failed messages in a batch.<br>+ Handle partial failure: only failed messages get retried.<br>+ Integrate with SQS event source mapping. | 09/07/2026 | 09/07/2026 | |
| Thu | - Test retry and DLQ:<br>+ Deliberately send faulty messages to test the retry mechanism.<br>+ Verify messages are retried exactly 3 times.<br>+ Verify messages are moved to DLQ after all retries fail. | 10/07/2026 | 10/07/2026 | |
| Fri - Sat | - Set up CloudWatch Metrics and Alarms for DLQ:<br>+ Create ApproximateNumberOfMessagesVisible metric for DLQ.<br>+ Set up CloudWatch Alarm when DLQ has messages (threshold > 0).<br>+ Configure SNS notification to send email/alerts when alarm triggers. | 11/07/2026 | 12/07/2026 | |

### Week 10 Results:

* Successfully built Dead Letter Queue system to manage failed messages in asynchronous processing.
* Configured RedrivePolicy with maxReceiveCount = 3, messages automatically move to DLQ after 3 failed retries.
* Created dedicated DLQ queues per service (game-economy-dlq.fifo) with 14-day retention period.
* Successfully configured ReportBatchItemFailures for partial failure handling in batch processing.
* Retry testing successful: failed messages are retried exactly 3 times before moving to DLQ.
* Set up CloudWatch Metrics and Alarms to monitor DLQ, sending alerts via SNS when failed messages are detected.
