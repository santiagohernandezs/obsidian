---
tags:
  - cloud
  - google
aliases:
---

# Cloud Computing
## What is cloud computing?
US National Institute of Standards and Technology created the term "cloud computing", as a way of using information technology that has these five equally important traits.
1. Customers get computing resources that are on-demand and self-service. Through a web interface users get the processing power, storage, and network they need with no need for human interaction.
2. Customers get access to those resources over the internet, from anywhere they have a connection.
3. The provider of those resources allocates them to users out of that pool.
4. The resources are elastic - which means they can increase or decrease as needed, so customers can be flexible.
5. Customers pay only for what they use, or reserve as they go.
## What is an infrastructure
 An infrastructure is the basic underlaying framework of facilities and systems
 ![[Pasted image 20230916121355.png|525]]
## Cloud vs. Traditional architecture
To understand the comparation we need to look at some history. The trend toward cloud computing is separated in three waves:
1. First wave, Colocation: This gave the financially efficiency to the users of renting physical space, instead of investing in data center real estate.
2. Second wave, Virtualized data center: Shares similarities with private data centers and colocations, now all the infrastructure (server, CPUs, disks, load balancers...) are virtual devices, keeping the infrastructure with a user-controlled and user-configured environment.
3. Third wave, Container-based architecture: A fully automated-elastic cloud that consist in automated services and scalable data. Services automatically provision and configure the infrastructure used to run applications.
## IaaS, PaaS, and SaaS
- IaaS - Infrastructure as a service: Provide raw compute, storage and network capabilities. The users pay for what they allocate.
- PaaS - Platform as a service: Binds the code to a library that provide access to the infrastructures applications need. More resources are in application logic. The users pay for what they use.
- SaaS - Software as a service: Saas applications are not installed in the client's computer, they run in the cloud as a service and can be consume through internet by end users.
## Google Cloud Architecture
	![[Pasted image 20230916135502.png|450]]

We can think about Google cloud architecture in three layers, the base layer is Networking and Security layer, which lays the foundation of support all fo Google's infrastructure and applications. The next one sit compute and storage, Google separates, or decouples compute and storage so they can scale independently based on need, and top Layer sit the big data and machine learning products, which enable you tasks to ingest, store, process, and deliver business insights, data pipelines, and machine learning models.
## Google Cloud computing services
![[Pasted image 20230916135848.png|700]]

## Google Cloud storage services
![[Pasted image 20230916140000.png|700]]

## Big Data and ML product line
![[Pasted image 20230916140108.png|600]]