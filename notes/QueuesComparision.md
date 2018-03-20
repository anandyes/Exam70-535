## Storage Queues vs. Service Bus Queues


|||
|:---|:---|
| **Storage Queues** |  **Service Bus Queues** |
| Arbitrary ordering |  FIFO guaranteed ordering |
| Delivery at least once, possible multiple times|  Delivery at least once and at most once |
| 30 second default locks can be extended to 7 days | 60 seconds default locks can be renewed |
| Supports in-place updates of the message content | Messages are finalized once consumed |
| Can integrate with WF through a custom activity | Native integration with WCF and WF|
| | |





