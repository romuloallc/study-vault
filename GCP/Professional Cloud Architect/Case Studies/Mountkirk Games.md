Subject: [[Google Cloud Platform]] #gcp  
#### Company overview
- Makes online, session-based, multiplayer games for mobile platforms;
- Start to expanding to other platforms after migrating to Google Cloud;
#### Solution concept
- Deploy the games's backend on GKE;
- Use global Load Balancer to route players to the closest regional game arenas;
- Global leader border in sync, they plan to use a multi-region Spanner cluster;
#### Existing technical environment
- Each new game exists in isolated project nested below a folder;
- Legacy games with low traffic have been consolidated into a single project;
- Separate environments for development and testing;
#### Business requirements
- Support multiple gaming platforms;
- Support multiple regions;
- Support rapid iteration of game features;
- Minimize latency;
- Optimize for dynamic scaling;
- Use managed services and pooled resources;
- Minimize costs;
#### Technical requirements
- Dynamically scale based on game activity;
- Publish scoring data on a near real-time global leaderborder;
- Store game activity logs in structured files for future analysis;
- Use GPU processing to render graphics server-side for multi-platform support;
- Support eventual migration of legacy games to this new platform;