# Steps
# Step 1: Scope the problem
Answer this questions to define the problem and clarify ambiguities before diving deep into specific parts of the system we will focus on later.

- Why do we need this? 
- Who is our user?
- What can users do?
- What can users see/get/list (display) ?
- What data is handled with requests/response: text, multimedia, size limits? 
- How is data processed? (#steps?)
- Push vs. pull features 
- Back-end vs Front-end features
- What clients should be available? (CLI, Rest, Web Browser, Desktop, Mobile) 

# Step 2: System interface definition (API design)
- API design
- API definition - contract
- Initial traffic constraints (read vs write APIs)

# Step 3: Data model definition
This will help define the data flow among components, as well as chances for data partitioning, management (storage, transport, encryption, etc), monitoring.

- What are the main entities, and its attributes?
- What are the relationships between entities? 
- Are all interactions/features represented in the data? 
- Is there semi-structured or unstructured data? 
- Is the schema stable or fixed or should it be flexible? 

# Step 4: Sizing estimation
This will help when we focus on scaling, partitioning, load balancing, caching, etc.

Estimates for: 
- Number of requests (Create | Get | List , etc) per unit of time (days | months | sec. , etc)
- Read/write requests ratio
- Storage we need per type of media (text, IDs, user info, image, video, etc)
- Bandwidth usage needs / limitations - consider where your users are located.

# Step 5: High-level design
Draw the core components of the system that address all features end-to-end.

# Step 6: Detailed design
Analyze the components, identify potential bottlenecks or services that need improvements/decomposition/detailed analysis in the system. 

Identify and mitigate or resolve bottlenecks
- Single points of failure - SPOFs
- Service availability risks
- Data availability risks
- Data integrity risks (do we need a disaster recovery plan?)
- Service failure risks - per component and in aggregate. 
- Performance degradation risks - Monitoring strategy
- Monitoring and alerting strategy

Iterate over each component
- Consider different approaches or designs; pros, cons, trade-offs
- Data partitioning
- Data usage patterns 
- Caching
- Load balancing, etc
- Decide on an approach, pros, cons, potential issues it introduces, trade-offs.
- Design observability of system’s health - per component of aggregate.