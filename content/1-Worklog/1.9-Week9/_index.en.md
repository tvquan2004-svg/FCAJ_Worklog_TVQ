---
title: "Worklog Week 9"
date: 2026-06-29
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Build an asynchronous processing system with SQS FIFO to ensure transaction order.
* Configure Producer Lambda to send messages to the SQS queue.
* Build Consumer Lambda to receive and process messages from SQS.
* Implement pessimistic locking in transactions to prevent race conditions.

### Weekly Tasks:

| Day | Tasks | Start Date | End Date | Resources / Notes |
| --- | --- | --- | --- | --- |
| Mon | - Learn SQS FIFO mechanism:<br>+ Compare Standard Queue vs FIFO Queue.<br>+ How FIFO ensures message order (First-In-First-Out).<br>+ Message Group ID and Deduplication ID. | 30/06/2026 | 30/06/2026 | |
| Tue | - Configure Producer Lambda:<br>+ Integrate AWS SDK to send messages to SQS FIFO.<br>+ Set Message Group ID by player ID to ensure transaction order per player.<br>+ Handle send errors and retry logic. | 01/07/2026 | 01/07/2026 | |
| Wed | - Build Consumer Lambda:<br>+ Configure SQS trigger for Lambda.<br>+ Process received messages from the queue.<br>+ Implement pessimistic lock in transactions to prevent duplicate processing. | 02/07/2026 | 02/07/2026 | |
| Thu | - Implement pessimistic locking:<br>+ Use database-level locking (SELECT FOR UPDATE).<br>+ Ensure consistency when multiple messages process the same resource.<br>+ Handle timeout and rollback on lock failure. | 03/07/2026 | 03/07/2026 | |
| Fri - Sat | - Test the asynchronous system:<br>+ Send multiple concurrent messages, verify processing order.<br>+ Verify pessimistic lock works correctly.<br>+ Test error handling and retry. | 04/07/2026 | 05/07/2026 | |

### Week 9 Results:

* Mastered SQS FIFO architecture and its application in the game transaction system to ensure processing order.
* Successfully built Producer Lambda sending messages to SQS FIFO with Message Group ID per player.
* Consumer Lambda configured with SQS trigger, automatically processing messages when new data arrives.
* Implemented pessimistic lock (SELECT FOR UPDATE) in transactions, ensuring no race conditions when processing multiple concurrent transactions on the same resource.
* Asynchronous processing system operates stably, ensuring transaction order and data consistency.
