Version:NAFATH-V2
Networking

## Overview 
A telecommunications operator launching a 5G service for emergency responders must ensure reliable, secure, and continuous communication during network congestion, outages, and cyberattacks, enabling teams to coordinate efficiently. Six IT fields collaborate to achieve this:Software Engineering develops reliable applications that queue data during offline periods and re-sync seamlessly without duplication upon reconnection.Networking provides high-speed connectivity by reserving bandwidth via network slicing, prioritizing urgent traffic, and switching to backup connections during outages.Cybersecurity protects systems through encryption, authentication, and continuous monitoring to ensure data confidentiality and availability.Artificial Intelligence analyzes data to predict congestion, detect anomalies, and provide recommendations for faster decision-making.Mobile Technology equips responders with 5G smart devices to access applications and share live video, voice calls, and location data.Data Management collects and stores information to ensure it remains accurate, secure, and accessible.Integrating these six fields helps the operator maintain service availability, protect critical communications, and support effective emergency response when reliable connectivity is essential.

## Software
Safe and Idempotent HTTP Methods
Safe Methods: GET and HEAD retrieve information without changing server data.
Idempotent Methods: GET, PUT, and DELETE produce the same final result when repeated.
Why does this matter when a client automatically retries a request that failed?
* GET, PUT, DELETE: Can usually be retried safely because repeating them does not change the final result.
* POST: Retrying may create duplicate records or charge a user twice if the first request succeeds but its response is lost. Therefore, POST requests need careful retry handling to avoid unintended actions.

Resource: <HTTP Methods and Idempotency> - https://algomaster.io/learn/computer-networks/http-methods-and-idempotency

 ## AI:
Overfitting: Happens when a machine learning model memorizes training data instead of learning real network traffic patterns, leading to poor performance on live 5G networks.
Cross-Validation: Divides data into groups. The model trains on some groups and validates on another, repeating this process.
Detection: If training accuracy is high but validation accuracy is low, the model may be overfitting. Data scientists can then improve the model before using it in real networks.

Resource: <Overfitting in Machine Learning: How to Detect and Prevent It> - https://medium.com/@petraclara20/overfitting-in-machine-learning-how-to-detect-and-prevent-it-5ae4ed2ec7e4

## Mobile 
When emergency responders enter areas without network coverage, the mobile application should continue working offline and sync data when the connection returns.
* Local Storage: Saves important information, such as maps and forms, on the device.
* Action Queuing: Stores offline data until it can be sent to the server.
* Background Sync: Retries sending data when the network returns.
* Duplicate Prevention: Uses unique IDs to prevent repeated submissions.
* Conflict Resolution: Applies rules to handle different versions of updated data.
  
 Resource:< Build an offline-first app> - https://developer.android.com/topic/architecture/data-layer/offline-first

## Networking
5G network slicing allows a telecom operator to create separate virtual networks using the same infrastructure. Each network can be designed for a specific purpose.
For emergency responders, it provides a dedicated and secure network connection. This helps reduce the impact of public network congestion and gives emergency services higher priority. It also supports reserved bandwidth, faster data transmission, and low latency for body cameras and live video streaming. These features help emergency teams communicate reliably during major incidents and natural disasters.

Resource:< 5G networking slicing> - https://www.premierwireless.com/blog/5g-network-slicing-explained-what-it-means-for-first-responder-communications

## Cybersecurity
The Incident Response Lifecycle has six main phases that help organizations handle security incidents effectively.
1. Preparation: Train the team, create security policies, and practice response plans.
2. Identification: Detect the attack, find its possible source, and identify the affected systems.
3. Containment: Isolate affected devices to stop the attack from spreading and protect digital evidence.
4. Eradication: Remove malware, fix security vulnerabilities, and solve the main cause of the incident.
5. Recovery: Restore clean systems and monitor them to make sure they are working safely.
6. Lessons Learned: Review the incident, identify weaknesses, and improve security measures for the future.

Resource:< incident response phases> - https://www.securitymetrics.com/blog/6-phases-incident-response-plan

## Data
To report service usage by region and day, it is important to understand the difference between Star Schema and Snowflake Schema.
* Star Schema: It has a central fact table connected directly to dimension tables. This makes queries simpler and usually faster.
* Snowflake Schema: It divides dimension tables into smaller tables. This helps reduce data duplication and save storage space, but queries can become more complex.
Best choice: Star Schema is suitable for regional and daily reports because it requires fewer JOIN operations. This helps retrieve data faster and makes reporting easier and more efficient.

Resource:< star schema vs snowflake>https://www.coursera.org/articles/star-schema-vs-snowflake-schema
