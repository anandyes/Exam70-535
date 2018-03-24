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

|||
|:--|:--|
| **Azure Service Bus Queues** |  **Azure Storage Queues** |
| Message lifetime >7 days | Message lifetime <7days |
| Guaranteed (first in–first out) ordered |  Queue size >80 GB |
| Duplicate detection | Transaction logs |
| Message size ≤1 MB | Message size ≤64 KB |
|||


### When to use which Azure service for messages or events

||||||||
|:--|:--|:--|:--|:--|:--|:--|
|  | Event Grid | Event Hubs | IoT Hub | Topics |Service Bus Queues | Storage Queues |
|Event ingestion | X | X | X |
|Device management| | | X | | | |
|Messaging|X|X|X|X|X|X|
|Multiple consumers|X| X| X| X| | |
|Multiple senders |X |X |X |X |X |X |
|Use for decoupling| |X |X |X |X |X |
|Use for publish/subscribe| X |
|Max message size| 64 KB |256 KB| 256 KB| 1 MB| 1 MB| 64 KB |
||||||||