Subject: [[Google Cloud Platform]] #gcp  
#### Company overview
- Global sports league for competitive helicopter racing;
- Each year HRL holds world championship and several regional league competitions;
- HRL offers a paid service to stream the races all over the world with live telemetry and predictions throughout each race;
#### Solution concept
- Wants to migrate their existing service to a new platform to expand their use of managed AI and ML services to facilitate race predictions;
- Additionally, as new fans engage with the sport, particularly in emerging regions, they want to move the serving of their content, both real-time and recorded, closer to their users;
#### Existing technical environment
- HRL is a public cloud-first company;
- Video recording and editing is performed at the race tracks, and the content is encoded and transcoded, where needed, in the cloud;
- Enterprise-grad connectivity and local compute is provided by truck-mounted mobile data centers;
- Their race prediction services are hosted on their existing public cloud provider;
- Existing technical environment is as follows:
	- Existing content is stored in an object storage service on their existing public cloud provider;
	- Video encoding and transcoding is performed on VMs created for each job;
	- Race predictions are performed using TensorFlow running on VMs in the current public cloud provider;
#### Business requirements
- Support ability to expose the predictive models to partners;
- Increase predictive capabilities during and before races:
	- Race results;
	- Mechanical failures;
	- Crow sentiment;
- Increase telemetry and create additional insights;
- Measure fan engagement with new predictions;
- Enhance global availability and quality of the broadcasts;
- Increase the number of concurrent viewers;
- Minimize operational complexity;
- Ensure compliance with regulations;
- Create a merchandising revenue stream;
#### Technical requirements
- Maintain or increase prediction throughput and accuracy;
- Reduce viewer latency;
- Increase transcoding performance;
- Create real-time analytics of viewer consumption patterns and engagement;
- Create a data mart to enable processing of large volumes of race data;