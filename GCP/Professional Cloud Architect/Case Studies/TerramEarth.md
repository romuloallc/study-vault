Subject: [[Google Cloud Platform]] #gcp  
#### Overview
- Manufactures *heavy equipment for the mining and agricultural industries*;
- *500 dealers and service centers in 100 countries*;
#### Solution concept
- *2 million vehicles in operation currently*;
- Vehicles **collect telemetry data from many sensors during operation**;
- **Small subset of critical data is transmitted from the vehicles in** ==real time== to facilitate fleet management;
- Rest of the sensor ==data is collected, compressed, and uploaded daily== when the vehicles return;
- Each vehicle usually **generates 200 to 500 MB per day**;
#### Existing technical environment
 - Vehicle ==data aggregation and analysis infrastructure== resides in ==Google Cloud== and **servers clients from all around the world**;
 - ==Growing amount of sensor data== is captured from their **two main manufacturing plants and ==sent== to private data centers** that contain their ==legacy inventory and logistics management systems==;
 - Private data centers have ==multiple network inteconnects== configured to Google Cloud;
 - ==Web frontend== for dealers and customers ==is running in Google Cloud== and allows access to stock management and analytics;
#### Business requirements
 - Predict and detect vehicle malfunction for just-in-time repair where possible;
 - Decrease cloud operational costs and adapt to seasonality;
 - Increase speed and reliability of development;
 - Allow remote developers to be productive without compromising code or data security;
 - Create flexible and scalable platform for developers to create custom API services;
#### Technical requirements
- New abstraction layer for HTTP API access to their legacy systems to enable a gradual move into the cloud; (LB -> Hybrid NEG)
- Modernize all CI/CD pipelines to allow developers to deploy container-based workloads in highly scalable environments; (Kubernetes)
- Allow developers to run experiments without compromising security and governance requirements; (IAM + Kubernetes DEV)
- Create self-service portal for internal and partner developers to create new projects, request resources for data analytics jobs, and centrally manage access to the API endpoints; (Cloud Run?)
- Cloud-native solutions for keys and secrets management and optimize for identity-based access; (Secret manager + IAM)
- Improve and standardize tools for application and network monitoring and troubleshooting; (Logging + Monitoring)
