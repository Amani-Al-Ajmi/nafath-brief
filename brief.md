## software
Safe and Idempotent HTTP Methods
Safe Methods: GET and HEAD retrieve information without changing server data.
Idempotent Methods: GET, PUT, and DELETE produce the same final result when repeated.
Why Retries Matter:
* GET, PUT, DELETE: Can usually be retried safely because repeating them does not change the final result.
* POST: Retrying may create duplicate records or charge a user twice if the first request succeeds but its response is lost. Therefore, POST requests need careful retry handling to avoid unintended actions.
  
Resource:< HTTP Methods and Idempotency> - https://algomaster.io/learn/computer-networks/http-methods-and-idempotency

 ## AI:
AI: Overfitting and Cross-Validation
* Overfitting: Happens when a machine learning model memorizes training data instead of learning real network traffic patterns, leading to poor performance on live 5G networks.
* Cross-Validation: Divides data into groups. The model trains on some groups and validates on another, repeating this process.
* Detection: If training accuracy is high but validation accuracy is low, the model may be overfitting. Data scientists can then improve the model before using it in real networks.

Resource:< Overfitting in Machine Learning: How to Detect and Prevent It> - https://medium.com/@petraclara20/overfitting-in-machine-learning-how-to-detect-and-prevent-it-5ae4ed2ec7e4

## Mobile 
When emergency responders enter areas without network coverage, the mobile application should continue working offline and sync data when the connection returns.
* Local Storage: Saves important information, such as maps and forms, on the device.
* Action Queuing: Stores offline data until it can be sent to the server.
* Background Sync: Retries sending data when the network returns.
* Duplicate Prevention: Uses unique IDs to prevent repeated submissions.
* Conflict Resolution: Applies rules to handle different versions of updated data.
  
 Resource:< Build an offline-first app> - https://developer.android.com/topic/architecture/data-layer/offline-first
