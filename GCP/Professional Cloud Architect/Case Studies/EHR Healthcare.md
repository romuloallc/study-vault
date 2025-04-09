Subject: [[Google Cloud Platform]] #gcp  
#### Company Overview
- Eletronic health record software to the medical industry;
- Software as a Service (SaaS) to multi-national medical offices, hospitals, and insuranve providers;
#### Solution concept
- Need to be able to scale their environment;
- Adapt their disaster recovery plan;
- Roll out new continuous deployment capabilities to update their software at a fast pace;
- GCP has been chosen to replace their current colocation facilities;
#### Existing technical environment
- Multiple colocation facilities. The lease on one of the data centers is about to expire;
- Customer-facing applications are web-base, and many have recently been containerized to run on Kubernetes clusters;
- Data is stored in a mix of relational and NoSQL databases;
- Several legacy file-based and API-based integrations with insuranve providers on-premises. These systems are scheduled to be replaced over the next several years;
- Users are managed via Microsoft Actve Directory;
- Monitoring is done via various open source tools;
- Alerts are sent via email and are often ignored;
#### Business requirements
- On-board net insurance providers as quickly as possible;
- Provide a minimum 99,9% availability for all customer-facing systems;
- Centralized visibility and proactive action on system performance and usage;
- Increase ability to provide insights into healthcare trends;
- Reduce latency to all customers;
- Maintain regulatory compliance;
- Decrease infrastructure administration costs;
- Make predictions and generate reports on industry trends based on provider data;
#### Technical requirements
- Maintain legacy interfaces to insurance providers with connectivity on-premises/cloud providers;
- Provide a consistent way to manage customer-facing applications that are container-based;
- Provide a secure and high-performance connections between on-premises systems and GCP;
- Provide consistent logging, log retention, monitoring, and alerting capabilities;
- Maintain and manage multiple container-based environments;
- Dynamically scale and provision new environments;
- Create interfaces to ingest and process data from new providers;
