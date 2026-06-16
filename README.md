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
