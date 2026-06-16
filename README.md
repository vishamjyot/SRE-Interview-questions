For revision purposes, a clean Question → Answer format is much easier to memorize. I have only reorganized your content into Q&A format and improved readability without adding new content.

⸻

SRE, Linux & Networking Interview Notes

Q1. What is an SLI (Service Level Indicator)?

Answer:

An SLI is a measurement or metric that tells you how your service is performing.

⸻

Q2. What is an SLO (Service Level Objective)?

Answer:

An SLO is a goal or target for the SLI.

Think of it as:

🎯 What reliability level you aim for.

An SLO defines what acceptable performance is.

Examples:

* Availability: 99.95% monthly
* Latency: 95% of requests < 300ms
* Error Rate: < 0.1% per day
* Freshness: 99.9% data replication within 5 seconds

⸻

Q3. What is an SLA (Service Level Agreement)?

Answer:

An SLA is a formal contract with customers that includes consequences (usually financial) if the SLO is not met.

⸻

Q4. What is a cgroup in Linux?

Answer:

A cgroup (Control Group) in Ubuntu/Linux is a kernel mechanism that limits, accounts, and isolates CPU, memory, and I/O usage of processes.

It is the foundation for systemd services and containers.

⸻

Q5. What is OverlayFS?

Answer:

(Answer Pending)

⸻

Q6. How do we segregate the network in Linux?

Answer:

(Answer Pending)

⸻

Q7. What is a Hash in Redis?

Answer:

Without Redis hashes, you cannot store multiple fields under the same key; you must create separate keys.

Hashes exist to model structured data under a single Redis key.

⸻

Q8. What is a Data Structure? Elaborate some of them.

Answer:

A data structure is a way of organizing and storing data in a computer so that it can be accessed and manipulated efficiently.

Types:

* Arrays
* Linked Lists
* Stacks
* Trees
* Heaps
* Hash Tables

⸻

Q9. What is the difference between a Process and a Thread?

Answer:

Process

A process is an independent program in execution with its own memory space.

Thread

A thread is a lightweight execution unit within a process, sharing the process’s resources.

⸻

Q10. What are Error Budgets and what are they used for?

Answer:

An error budget is how much downtime a system can afford without upsetting consumers.

It is also known as the margin of error permitted by the Service Level Objective (SLO).

It encourages teams to minimize actual incidents.

⸻

Q11. Which activities help reduce toil?

Answer:

Activities that reduce toil include:

* Creating external automation
* Creating internal automation
* Enhancing the service so it does not require maintenance intervention

What is Toil?

Toil is:

* Repetitive
* Manual
* Automatable
* Tactical (interrupt-driven)
* Non-strategic work

Examples:

* Constant alert acknowledgment
* Manual server restarts
* Repetitive data extraction

⸻

Q12. List some Linux Signals.

Answer:

Signal	No.	Purpose	Can Handle?
SIGHUP	1	Reload config	Yes
SIGINT	2	Interrupt	Yes
SIGQUIT	3	Quit + core	Yes
SIGFPE	8	Math error	Yes
SIGKILL	9	Force kill	No
SIGALRM	14	Timer expired	Yes
SIGTERM	15	Graceful stop	Yes

⸻

Q13. What is DHCP and its use?

Answer:

DHCP (Dynamic Host Configuration Protocol) is a network management protocol used to automatically assign IP configuration to devices on a network.

⸻

Q14. Explain the difference between SNAT and DNAT.

Answer:

SNAT

Modifies the source IP of outbound packets so private hosts can access external networks.

DNAT

Modifies the destination IP of inbound packets to route traffic to internal services.

⸻

Q15. What are the benefits of Multithreading?

Answer:

* Parallel Execution
* Improved Performance
* Better Resource Utilization
* Better User Experience
* Scalability
* Modularity

⸻

Q16. What does a Playbook refer to in SRE?

Answer:

A playbook is a documented set of standardized steps used to handle specific operational tasks or incidents.

⸻

Q17. What is Chaos Engineering?

Answer:

Chaos engineering is the practice of deliberately introducing failures to test and improve system resilience.

Why it is used:

* Expose hidden weaknesses before real outages occur
* Validate redundancy, failover, and SLOs
* Build confidence in system reliability

Typical Experiments:

* Killing processes or pods
* Injecting network latency or packet loss
* Simulating node or zone failures
* Throttling CPU, memory, or I/O

⸻

Q18. What is Capacity Planning and why is it important?

Answer:

Capacity planning is the forecasting of resource needs in the future based on current usage trends and expected growth.

It ensures that a system can handle increased traffic or demand without performance degradation.

⸻

Q19. What is the importance of Postmortems in SRE?

Answer:

Postmortems are critical because they turn incidents into learning and reliability improvements rather than repeated failures.

⸻

Q20. How do you handle On-Call Responsibilities?

Answer:

On-call responsibilities involve readiness to react to incidents within a certain time.

I make sure I have monitoring tools available and am aware of escalation paths.

While on call, I focus on:

* Finding the root cause
* Resolving issues quickly
* Ensuring smooth handover when required

⸻

Q21. Explain the difference between Proactive and Reactive Monitoring.

Answer:

Proactive Monitoring

Detects and addresses issues before they impact users.

Reactive Monitoring

Responds to incidents after they have occurred.

⸻

Q22. What is Incident Management in SRE?

Answer:

Incident management involves:

* Detecting incidents
* Responding to incidents
* Resolving incidents

Its goal is to minimize service impact and restore services quickly.

⸻

Q23. What is the significance of Automation in SRE?

Answer:

Automation helps:

* Reduce manual tasks
* Minimize human errors
* Increase efficiency
* Ensure consistency across infrastructure

⸻

Q24. How do you handle On-Call Rotations?

Answer:

On-call rotations are managed by:

* Scheduling engineers for incident response
* Maintaining proper documentation
* Providing necessary training

⸻

Q25. What is Microservices Architecture?

Answer:

Microservices architecture breaks a monolithic application into smaller, independently deployable services.

Each service is responsible for a specific functionality.

⸻

Q26. How do you manage Configuration Drift?

Answer:

Configuration drift is managed through:

* Automation
* Regular audits
* Infrastructure as Code (IaC)

⸻

Q27. What is a Service Mesh?

Answer:

A service mesh is a dedicated infrastructure layer that manages service-to-service communication.

Features include:

* Load balancing
* Service discovery
* Security

⸻

Q28. What is a Failover System?

Answer:

A failover system automatically switches to a backup system when the primary system fails.

This ensures continuous availability.

⸻

Q29. Explain Defense in Depth.

Answer:

Defense in depth is a layered security approach where multiple security measures are implemented.

If one layer fails, others continue providing protection.

⸻

Q30. How do you handle Noisy Neighbors in a Multi-Tenant Environment?

Answer:

* Set CPU and memory limits
* Use cgroups
* Implement QoS policies
* Monitor resource usage

⸻

Q31. What is Load Shedding?

Answer:

Load shedding intentionally drops or refuses some requests during overload conditions.

Its purpose is to protect core functionality and prevent complete failure.

⸻

Q32. What is the Circuit Breaker Pattern?

Answer:

The circuit breaker pattern detects failures and prevents cascading failures.

It temporarily blocks requests to a failing service and allows recovery before resuming traffic.

⸻

Q33. How do you perform a Fault Injection Test?

Answer:

Fault injection deliberately introduces failures to test resilience.

Examples:

* Network failures
* Server crashes
* High latency

Tools:

* Chaos Monkey
* Gremlin

⸻

Q34. What is a Shadow Deployment?

Answer:

A shadow deployment deploys a new version alongside the current version and mirrors production traffic to it without impacting users.

⸻

Q35. What is Throttling?

Answer:

Throttling limits the number of requests a service can handle.

It prevents overload and ensures fair resource allocation.

⸻

Q36. What are key metrics for Microservices?

Answer:

* Latency
* Throughput
* Error Rate
* Request Rate
* CPU Utilization
* Memory Utilization

⸻

Q37. What is Graceful Degradation?

Answer:

Graceful degradation allows a system to continue operating with reduced functionality during partial failures.

⸻

Q38. How do you manage Secrets in a Cloud-Native Environment?

Answer:

* Kubernetes Secrets
* HashiCorp Vault
* AWS Secrets Manager
* Azure Key Vault

⸻

Q39. Difference between Active-Active and Active-Passive Failover?

Answer:

Active-Active

Multiple systems actively serve traffic.

Active-Passive

One active system serves traffic while a standby system takes over during failure.

⸻

Q40. What is the significance of Load Testing?

Answer:

Load testing simulates high traffic conditions to:

* Evaluate performance
* Identify bottlenecks
* Validate scalability

⸻

Q41. What is a Synthetic Transaction?

Answer:

A synthetic transaction is a scripted sequence of interactions that mimics real user behavior.

It is used to monitor availability and performance.

⸻

Q42. What is a Service Registry?

Answer:

A service registry is a dynamic database of service instances and their locations used for service discovery.

⸻

Q43. What is the purpose of an Alerting System?

Answer:

An alerting system notifies engineers of issues in real time so incidents can be addressed quickly.

⸻

Q44. How do you ensure Data Integrity in Distributed Systems?

Answer:

* Transaction management
* Data replication
* Consistency checks
* Consensus algorithms (Raft, Paxos)

⸻

Q45. What is the significance of a Distributed Cache?

Answer:

A distributed cache:

* Reduces database load
* Decreases latency
* Improves scalability
* Speeds up data retrieval

⸻

Q46. How does a Process become a Zombie Process?

Answer:

A zombie process is a process whose execution has completed but still has an entry in the process table.

This happens when the parent process does not execute wait() after forking.

⸻

Q47. Explain atime, mtime, and ctime.

Answer:

atime

Last access time.

mtime

Last modification time.

ctime

Time when inode metadata changed (permissions, ownership, etc.).

⸻

Q48. What is /proc Filesystem?

Answer:

/proc is a virtual filesystem that exposes kernel data structures and system information.

It provides information about:

* Processes
* Hardware
* Memory
* CPU
* Kernel parameters

⸻

Q49. How will you secure Docker Containers?

Answer:

* Choose third-party containers carefully
* Enable Docker Content Trust
* Set resource limits
* Consider third-party security tools
* Use Docker Bench Security

⸻

Q50. What is the difference between Monitoring and Observability?

Answer:

Monitoring

“What is wrong?”

Observability

“Why is it wrong?”

Monitoring tells you when something is broken.

Observability helps you understand why it is broken.

⸻

Q51. Your Web Application is Loading Slowly. What Steps Would You Take?

Answer:

1. Check latency and error metrics.
2. Review logs for timeouts and exceptions.
3. Use APM/tracing.
4. Investigate:
    * Database performance
    * Resource saturation
    * Traffic spikes

⸻

Q52. How do you ensure Zero-Downtime Deployments?

Answer:

* Rolling deployments
* Blue-Green deployments
* Canary deployments
* Readiness probes
* Liveness probes
* Health checks
* Circuit breakers
* Retries

⸻

Q53. Explain the Incident Response Lifecycle.

Answer:

1. Detection
2. Response
3. Communication
4. Resolution
5. Postmortem

⸻

Q54. Database Latency has Increased. What Would You Do?

Answer:

* Check DB CPU and memory usage
* Identify slow queries using EXPLAIN
* Review schema/index changes
* Analyze connection pool saturation

⸻

Q55. A Noisy Neighbor Pod is Impacting Others. What Steps Do You Take?

Answer:

* Set CPU/memory limits and requests
* Use node affinity
* Use taints and tolerations
* Isolate critical services
* Implement QoS classes

⸻

Q56. How Would You Handle an Incident in Production?

Answer:

1. Detect
2. Contain
3. Resolve

Use monitoring tools to identify issues, isolate affected components, and deploy fixes when needed.

⸻

Q57. You’re Onboarding a New Microservice. What Observability Steps Do You Take?

Answer:

* Define SLIs and SLOs
* Add metrics, logs, and traces
* Integrate monitoring tools
* Configure alerts
* Test with load and failure simulations

Golden Signals

* Latency
* Traffic
* Errors
* Saturation

⸻

Q58. Your Service Shows Latency Spikes Under Load. What Is Your Approach?

Answer:

* Profile using APM tools
* Analyze GC pauses
* Check thread contention
* Review DB/cache interactions
* Load test with k6 or JMeter
* Introduce caching and batching

⸻

Q59. You’re Getting Frequent Noisy Alerts. What Do You Do?

Answer:

* Tune thresholds
* Suppress low-priority alerts
* Deduplicate alerts
* Group alerts
* Rate-limit flapping alerts
* Prioritize actionable alerts

⸻

Q60. How Would You Create a Post-Incident Report?

Answer:

Include:

* Timeline of events
* Root cause analysis
* Incident impact
* Resolution steps

⸻

Q61. How Do You Manage Software Deployments to Minimize Risk?

Answer:

Use strategies such as canary releases where changes are rolled out to a small subset of users before full deployment.

⸻

Q62. How Do You Promote SRE Culture in a New Team?

Answer:

* Establish SLAs/SLOs early
* Share on-call duties
* Encourage blameless retrospectives
* Track toil and automate
* Celebrate reliability improvements

⸻

Q63. What Role Does Kubernetes Play in SRE?

Answer:

Kubernetes enables:

* Resilient deployments
* Scalability
* Automated rollouts
* High availability
* Self-healing pods

⸻

Q64. Designing Alerting for a Global E-Commerce App. What’s Your Strategy?

Answer:

* Region-specific synthetic checks
* Alert on symptoms
* Route alerts based on time zones
* Include SLO-based alerting
* Review alerts regularly

⸻

Q65. CloudFront vs Redis Cache

Answer:

CloudFront caches static and public HTTP responses at edge locations to absorb internet-scale traffic spikes.

Redis caches hot backend data such as:

* Sessions
* Database query results
* Rate-limit counters

This protects databases and improves application performance.


Kubernetes Architecture & API Groups Interview Notes

⸻

Worker Node Components

Q1. What components run on every Kubernetes Worker Node?

Answer:

The following components run on every worker node and execute workloads:

* kubelet
* kube-proxy
* Container Runtime
* CNI Plugin
* CoreDNS (cluster add-on)

⸻

Q2. What is kubelet?

Answer:

kubelet is the node agent that runs on every worker node.

Responsibilities

* Communicates with the API Server
* Starts Pods and Containers
* Monitors running workloads
* Ensures containers run as defined in Pod specifications

Key Point

👉 kubelet actually runs the workloads.

⸻

Q3. What is kube-proxy?

Answer:

kube-proxy implements Service networking inside Kubernetes.

Responsibilities

* Routes traffic from Services to Pods
* Maintains networking rules
* Uses iptables or IPVS

Key Point

👉 kube-proxy handles internal load balancing inside the cluster.

⸻

Q4. What is a Container Runtime?

Answer:

A Container Runtime is responsible for running containers on a worker node.

Examples

* containerd
* CRI-O
* Docker (legacy)

Responsibilities

* Pull container images
* Start containers
* Stop containers
* Manage container lifecycle

⸻

Q5. What is CNI (Container Network Interface)?

Answer:

CNI is responsible for Kubernetes pod networking.

Examples

* Calico
* Flannel
* Canal
* Cilium

Responsibilities

* Assign Pod IP addresses
* Enable Pod-to-Pod communication
* Implement Network Policies

⸻

Q6. What is CoreDNS?

Answer:

CoreDNS is the DNS server used inside Kubernetes clusters.

Responsibilities

* DNS resolution
* Service discovery

Example

A pod can access:

mysql.default.svc.cluster.local

instead of using IP addresses.

⸻

Kubernetes Workflow

Q7. How does Kubernetes work internally when creating a Pod?

Answer:

User → kube-apiserver
        ↓
      etcd
        ↓
Scheduler → assigns pod to node
        ↓
kubelet → starts container
        ↓
CNI → provides networking
        ↓
kube-proxy → service routing
        ↓
CoreDNS → service name resolution

Flow Explanation

1. User sends a request to the API Server.
2. API Server stores the desired state in etcd.
3. Scheduler selects a suitable worker node.
4. kubelet creates the Pod on the assigned node.
5. CNI assigns networking.
6. kube-proxy configures service routing.
7. CoreDNS provides DNS-based service discovery.

⸻

Kubernetes API Groups

Q8. What is apps/v1 API Group?

Answer:

The apps/v1 API group is used for workload controllers.

Resources

* Deployment
* ReplicaSet
* StatefulSet
* DaemonSet
* ControllerRevision

Why Separate?

Workload controllers evolved independently from core Kubernetes objects.

⸻

Q9. What is batch/v1 API Group?

Answer:

The batch/v1 API group is used for run-to-completion workloads.

Resources

* Job
* CronJob

Purpose

Execute tasks that complete and exit.

Examples:

* Database backup jobs
* Scheduled reports
* Data processing tasks

⸻

Q10. What is autoscaling/v2 API Group?

Answer:

The autoscaling/v2 API group is used for autoscaling resources.

Resources

* HorizontalPodAutoscaler (HPA)

Why Separate?

Autoscaling evolved independently from core workload resources.

⸻

Q11. What is networking.k8s.io/v1 API Group?

Answer:

The networking.k8s.io/v1 API group manages networking resources.

Resources

* Ingress
* NetworkPolicy
* IngressClass
* IPAddress
* ServiceCIDR

Why Separate?

Networking features evolved independently from core APIs.

⸻

Q12. What is rbac.authorization.k8s.io/v1 API Group?

Answer:

The rbac.authorization.k8s.io/v1 API group manages Role-Based Access Control.

Resources

* Role
* RoleBinding
* ClusterRole
* ClusterRoleBinding

Purpose

Control permissions and access within the cluster.

⸻

Q13. What is policy/v1 API Group?

Answer:

The policy/v1 API group contains policy-related resources.

Resources

* PodDisruptionBudget (PDB)

Purpose

Protect applications from excessive voluntary disruptions.

⸻

Q14. What is storage.k8s.io/v1 API Group?

Answer:

The storage.k8s.io/v1 API group manages storage resources.

Resources

* StorageClass
* CSIDriver
* VolumeAttachment
* CSIStorageCapacity
* VolumeAttributesClass

Why Separate?

Storage systems evolved independently and required dedicated APIs.

⸻

Q15. What is coordination.k8s.io/v1 API Group?

Answer:

The coordination.k8s.io/v1 API group is used for coordination and leader election.

Resources

* Lease

Use Cases

* kube-controller-manager leader election
* Scheduler leader election
* Controller leader election

⸻

Q16. What is admissionregistration.k8s.io/v1 API Group?

Answer:

The admissionregistration.k8s.io/v1 API group manages admission controllers and webhooks.

Resources

* MutatingWebhookConfiguration
* ValidatingWebhookConfiguration
* ValidatingAdmissionPolicy

Purpose

Intercept and validate requests before objects are created or modified.

⸻

Q17. What is apiextensions.k8s.io/v1 API Group?

Answer:

The apiextensions.k8s.io/v1 API group is used to extend Kubernetes.

Resources

* CustomResourceDefinition (CRD)

Purpose

Create custom resources beyond built-in Kubernetes objects.

Example

Database
KafkaCluster
RedisCluster

Custom resources can be created through CRDs.

⸻

Q18. What is apiregistration.k8s.io/v1 API Group?

Answer:

The apiregistration.k8s.io/v1 API group is used to extend the Kubernetes API Server.

Resources

* APIService

Purpose

Register external APIs with the Kubernetes API Server.

⸻

Q19. What is crd.projectcalico.org/v1?

Answer:

This API group contains Calico-specific Custom Resource Definitions (CRDs).

Resources

* IPPool
* BGPPeer
* GlobalNetworkPolicy
* FelixConfiguration

Why Does It Exist?

Calico registers its own CRDs to extend Kubernetes networking capabilities.

⸻

Q20. What is resource.k8s.io/v1 API Group?

Answer:

The resource.k8s.io/v1 API group supports Kubernetes Dynamic Resource Allocation.

Resources

* ResourceClaim
* DeviceClass
* ResourceSlice

Purpose

Manage specialized hardware and dynamic resources.

Examples:

* GPUs
* FPGAs
* AI Accelerators
* Custom Hardware Devices

⸻

Quick Revision Table

API Group	Common Resources
apps/v1	Deployment, StatefulSet, DaemonSet
batch/v1	Job, CronJob
autoscaling/v2	HorizontalPodAutoscaler
networking.k8s.io/v1	Ingress, NetworkPolicy
rbac.authorization.k8s.io/v1	Role, ClusterRole
policy/v1	PodDisruptionBudget
storage.k8s.io/v1	StorageClass, CSIDriver
coordination.k8s.io/v1	Lease
admissionregistration.k8s.io/v1	MutatingWebhook, ValidatingWebhook
apiextensions.k8s.io/v1	CustomResourceDefinition
apiregistration.k8s.io/v1	APIService
crd.projectcalico.org/v1	IPPool, BGPPeer
resource.k8s.io/v1	ResourceClaim, DeviceClass


Linux, Kubernetes, Kafka, ELK & Database Interview Notes

⸻

Linux

Q1. What is the difference between awk and sed?

Answer:

sed

Used for:

* Search and replace
* Simple text modifications
* Stream editing

awk

Used for:

* Processing structured data
* Calculations
* Parsing columns
* Report generation

Rule of Thumb

* Use sed for straightforward text replacement.
* Use awk when working with structured data and calculations.

⸻

Q2. How do you check connectivity between two servers if ping is disabled?

Answer:

If ICMP (ping) is disabled, use port-based connectivity tests.

Telnet

telnet 192.168.1.10 80

Netcat

nc -vz 192.168.1.10 80

Other Tools

* curl
* nmap
* wget

⸻

Q3. How do you configure a Cron Job for a different timezone?

Answer:

crontab -e

Example:

TZ="America/New_York" 0 2 * * * /path/to/script.sh
TZ="Europe/London" 0 2 * * * /path/to/script.sh
TZ="Asia/Tokyo" 0 2 * * * /path/to/script.sh

⸻

Q4. What is Heap Memory?

Answer:

Heap is the memory region used for dynamic memory allocation during program execution.

Characteristics:

* Allocated at runtime
* Managed by malloc/new
* Freed manually or by garbage collection

⸻

Q5. Common Linux Commands and Their Uses?

Answer:

File Operations

ls
cd
cp
mv
rm
mkdir
cat

Search & Text Processing

grep
find

Permissions

chmod
chown

Process Management

ps
htop
kill

Archiving

tar
gunzip

Networking

netstat
telnet
ssh
scp
wget

System Monitoring

df -h

Scheduling

crontab

⸻

Kubernetes

Q6. How do you view logs from specific containers in a multi-container Pod?

Answer:

Container 1

kubectl logs nginx-node-simple-pod -c nginx-container

Container 2

kubectl logs nginx-node-simple-pod -c node-container

⸻

Q7. How do you upgrade a Kubernetes Cluster?

Answer:

Step 1: Backup

* etcd snapshot
* Deployments
* Services
* ConfigMaps
* Secrets

Step 2: Upgrade Control Plane

* Upgrade kubeadm
* Upgrade kubelet
* Upgrade kubectl

Step 3: Upgrade Worker Nodes

Drain node:

kubectl drain <node-name>

Upgrade packages.

Uncordon node:

kubectl uncordon <node-name>

⸻

Q8. How do you maximize Kubernetes Cluster Availability?

Answer:

Highly Available Control Plane

* Minimum 3 control plane nodes
* Multiple availability zones
* Load balancer in front of API servers

Worker Nodes

* Multiple worker nodes
* Multi-AZ deployment

Pod Anti-Affinity

podAntiAffinity:
  requiredDuringSchedulingIgnoredDuringExecution:

Pod Disruption Budget

spec:
  minAvailable: 80%

Replicas and Autoscaling

kubectl autoscale deployment my-app \
  --cpu-percent=50 \
  --min=2 \
  --max=10

Highly Available Ingress Controller

Use multiple replicas.

HA Storage

* Replicated Persistent Volumes
* Multi-AZ storage

Resource Requests & Limits

Define CPU and Memory requests/limits.

Deployment Strategies

* Rolling Updates
* Canary Deployments

Backup

* etcd
* PVs
* Configurations

⸻

Q9. Why do we use StatefulSets?

Answer:

StatefulSets are used for stateful applications.

Examples:

* MySQL
* PostgreSQL
* Cassandra
* Kafka
* RabbitMQ

Benefits

Stable Identity

pod-0
pod-1
pod-2

Persistent Storage

Each pod gets its own Persistent Volume.

Ordered Deployment

Pods are created sequentially.

Stable DNS

Each pod receives a stable hostname.

⸻

Q10. Which Service Does a StatefulSet Use?

Answer:

StatefulSets use a Headless Service.

Purpose:

* Stable network identities
* Stable DNS records

⸻

Q11. How do you check Kubernetes Resources?

Answer:

Nodes

kubectl get nodes
kubectl describe node <node-name>
kubectl top nodes

Pods

kubectl get pods
kubectl get pods -n <namespace>
kubectl describe pod <pod-name>
kubectl top pod <pod-name>

Deployments

kubectl get deployments
kubectl describe deployment <deployment-name>
kubectl rollout status deployment <deployment-name>

Services

kubectl get services
kubectl describe service <service-name>

StatefulSets

kubectl get statefulsets
kubectl describe statefulset <statefulset-name>

Storage

kubectl get pv
kubectl get pvc
kubectl describe pvc <pvc-name>

Logs

kubectl logs <pod-name>
kubectl logs <pod-name> -c <container-name>

Quotas

kubectl get resourcequotas
kubectl describe resourcequota <quota-name>

⸻

Q12. How do you check which Service is using which Port?

Answer:

kubectl get services
kubectl describe service <service-name>
kubectl get services --all-namespaces

⸻

Q13. What are the default Kubernetes Namespaces?

Answer:

default
kube-system
kube-public
kube-node-lease

Example:

kubectl get svc -n default

⸻

Q14. Difference Between ReplicaSet and Replication Controller?

Answer:

Both maintain the desired number of Pods.

ReplicaSet

* apps/v1
* Supports set-based selectors
* Current standard

Replication Controller

* v1 API
* Equality-based selectors only
* Deprecated

⸻

AWS

Q15. What checks should be done before launching an EC2 Instance?

Answer:

Instance Type

* General Purpose
* Compute Optimized
* Memory Optimized
* Storage Optimized
* GPU Instances

AMI Selection

* Latest AMI
* Trusted source

Security

* Security Groups
* Key Pair
* IAM Role

Networking

* VPC
* Subnets

Storage

* EBS sizing
* Encryption

Availability

* Auto Scaling
* Load Balancer

Cost Optimization

* Spot Instances
* Reserved Instances
* Right Sizing

Protection

* Termination Protection

⸻

Kafka & Keycloak

Q16. What is Keycloak?

Answer:

Keycloak is an open-source Identity and Access Management (IAM) solution.

Features:

* Authentication
* Authorization
* SSO
* OAuth2
* OpenID Connect
* SAML

⸻

Q17. What is Kafka?

Answer:

Kafka is a distributed event-streaming platform used for real-time data processing.

Uses

* Event-driven architectures
* Log aggregation
* Real-time analytics

⸻

Q18. What is ZooKeeper’s Role in Kafka?

Answer:

ZooKeeper:

* Coordinates Kafka brokers
* Maintains cluster metadata
* Supports leader election
* Ensures high availability

⸻

Q19. Producer-Consumer Problem in Kafka

How do you ensure a producer’s request is consumed by a specific consumer?

Answer:

Use a unique message key.

Producer

Assign:

user-id
session-id

as the message key.

Consumer

Consume from the partition associated with that key.

⸻

Monitoring & Observability

Q20. How do you identify and collect Application Metrics?

Answer:

Types of Metrics

Performance Metrics

* Latency
* Throughput
* Error Rate

Resource Metrics

* CPU
* Memory
* Disk I/O

User Metrics

* Active Users
* Session Duration

Business Metrics

* Transactions
* Conversion Rate

Common Tools

* Prometheus
* Grafana
* ELK Stack
* Datadog

⸻

Q21. How would you scale a Logging Platform with High Availability?

Answer:

Log Sharding

Benefits:

* Scalability
* Better Performance
* High Availability

Log Rotation

* Archive old logs
* Delete expired logs

⸻

Q22. How do you optimize Application Performance using APM?

Answer:

Monitoring

* Response Time
* Throughput
* Error Rate

Profiling

* Slow Methods
* CPU Hotspots

Database Optimization

* Query Analysis
* Indexing

Caching

* Redis
* Memcached

Load Balancing

Distribute traffic evenly.

Frontend Optimization

* Compression
* Image Optimization
* CDN

Testing

* Load Testing
* Stress Testing
* A/B Testing

⸻

Q23. What do you check in Kibana APM when requests flow through Microservices?

Answer:

Service Maps

Visualize service dependencies.

Distributed Tracing

Track request flow across services.

Transaction Duration

Identify slow services.

Error Rates

Identify failing services.

HTTP Calls

Analyze service-to-service communication.

⸻

Q24. How do you troubleshoot Login Issues across 20 Microservices using Kibana?

Answer:

Understand Login Flow

Identify all services involved.

Analyze Distributed Traces

Track login requests.

Check Transaction Duration

Look for bottlenecks.

Review Error Logs

Identify failures.

Review HTTP Requests

Check service communication.

⸻

Q25. How do you identify request flow among 20 Microservices?

Answer:

Use:

Distributed Tracing

Provides end-to-end request visibility.

Service Maps

Visualizes communication between services.

Transaction Analysis

Shows slow or failing transactions.

⸻

Scheduling

Q26. Explain Taints, Tolerations and Node Affinity.

Taints

Applied to nodes.

Types:

* NoSchedule
* PreferNoSchedule
* NoExecute

Tolerations

Applied to Pods.

Allow pods to run on tainted nodes.

Node Affinity

Schedules Pods based on node labels.

Required (Hard Rule)

requiredDuringSchedulingIgnoredDuringExecution

Preferred (Soft Rule)

preferredDuringSchedulingIgnoredDuringExecution

⸻

Q27. Why use Taints/Tolerations when Node Affinity Exists?

Answer:

They solve different problems.

Node Affinity

Controls where Pods prefer or must run.

Examples:

* SSD nodes
* GPU nodes
* High-memory nodes

Taints/Tolerations

Control which Pods are allowed to run on nodes.

They complement each other.

⸻

CoreDNS

Q28. How do you troubleshoot CoreDNS overload?

Answer:

Check Logs

kubectl logs -n kube-system -l k8s-app=kube-dns

Monitor Metrics

Use:

* Prometheus
* Metrics API

Check Resources

Review CPU and Memory utilization.

Scale CoreDNS

Increase replicas.

⸻

EFK / ELK

Q29. Difference Between Fluent Bit and Logstash?

Fluent Bit

Answer:

* Lightweight
* High Performance
* Low CPU Usage
* Low Memory Usage
* Single Binary

Best for:

* Log forwarding
* Resource-constrained environments

⸻

Logstash

Answer:

* JVM-based
* Higher resource usage
* Rich processing features

Best for:

* Complex log transformations
* Log enrichment

⸻

Q30. Which Ports Does Elasticsearch Use?

Answer:

Client Communication

9200

Node-to-Node Communication

9300

⸻

Q31. How Does ELK/EFK Stack Work?

Answer:

Deployment Model

* Fluentd → DaemonSet
* Elasticsearch → StatefulSet
* Kibana → Deployment

Flow

Application Logs
        ↓
Fluentd (24224)
        ↓
Elasticsearch (9200)
        ↓
Kibana (5601)

Components

Fluentd

Collects logs.

Elasticsearch

Stores and indexes logs.

Elasticsearch is a NoSQL database built on the Lucene Search Engine.

Kibana

Provides visualization and log analysis.

⸻

Kubernetes Control Plane

Q32. What is kube-apiserver?

Answer:

The entry point to Kubernetes.

Responsibilities:

* Accept requests
* Validate requests
* Communicate with etcd

Flow:

kubectl → kube-apiserver → cluster

If API Server stops, the cluster becomes inaccessible.

⸻

Q33. What is etcd?

Answer:

etcd is a distributed key-value database.

Stores:

* Pods
* Services
* ConfigMaps
* Secrets
* Desired State

It is the source of truth for Kubernetes.

⸻

Q34. What is kube-scheduler?

Answer:

Responsible for assigning Pods to Nodes.

Scheduling decisions are based on:

* CPU
* Memory
* Affinity
* Anti-Affinity
* Taints
* Tolerations

⸻

Q35. What is kube-controller-manager?

Answer:

Runs controllers that continuously ensure actual state matches desired state.

Controllers Managed

* Node Controller
* ReplicaSet Controller
* Deployment Controller
* StatefulSet Controller
* DaemonSet Controller
* Job Controller
* Endpoint Controller
* Namespace Controller
* Service Account Controller
* PV/PVC Controller
* Garbage Collector Controller
* HPA Controller

Provides:

* Self-healing
* Automation
* Reconciliation

⸻

Q36. What is the Raft Consensus Algorithm?

Answer:

Raft is a leader-based consensus algorithm used by etcd.

Responsibilities

* Leader Election
* Log Replication
* Majority Quorum Agreement

Benefits:

* Consistency
* Reliability
* Fault Tolerance

⸻

Q37. What Happens When You Run kubectl apply?

Answer:

kubectl
   ↓
API Server
   ↓
etcd
   ↓
Controller Manager
   ↓
Scheduler
   ↓
Kubelet
   ↓
Container Runtime
   ↓
Kube-Proxy

Flow

1. kubectl sends request to API Server.
2. API Server validates request.
3. Desired state stored in etcd.
4. Controllers reconcile state.
5. Scheduler assigns node.
6. Kubelet starts Pod.
7. Container Runtime pulls image.
8. Kube-Proxy configures networking.

⸻

SQL

Q38. Types of SQL Joins?

Answer:

1. INNER JOIN
2. LEFT JOIN
3. RIGHT JOIN
4. FULL JOIN
5. CROSS JOIN
6. SELF JOIN

⸻

Q39. Query to Find Employees Who Did Not Make Sales in October

Answer:

SELECT e.*
FROM employees e
LEFT JOIN sales s
    ON e.employee_id = s.employee_id
    AND MONTH(s.sale_date) = 10
    AND YEAR(s.sale_date) = YEAR(CURDATE())
WHERE s.sale_id IS NULL;

⸻
