## Database related services in AWS 

https://aws.amazon.com/api-gateway/features/

| Service                                 | Description/Use Case                                                                                                                                                                                                                                                       |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amazon Aurora                           | Fully managed relational database engine compatible with MySQL and PostgreSQL. High performance, scalability, and availability.                                                                                                                                            |
| Amazon RDS                              | Fully managed relational database service supporting various engines like MySQL, PostgreSQL, Oracle, SQL Server, and MariaDB.                                                                                                                                              |
| Amazon DynamoDB                         | Fully managed NoSQL database service offering low-latency, high-throughput storage for structured data. Scalable and flexible.                                                                                                                                             |
| Amazon Neptune                          | Fully managed graph database service optimized for storing and querying highly connected data. Suitable for graph-based applications, social networking, recommendation engines, fraud detection, and knowledge graphs.                                                    |
| Amazon Redshift                         | Fully managed data warehousing service optimized for analyzing large datasets. Suitable for complex queries and analytics.                                                                                                                                                 |
| Amazon DocumentDB                       | Fully managed document database service compatible with MongoDB workloads. Supports JSON-like documents and scalable storage.                                                                                                                                              |
| Amazon QLDB                             | Fully managed ledger database service offering transparent, immutable, and cryptographically verifiable transaction logs. Suitable for applications requiring an immutable and transparent audit trail, such as financial auditing, supply chain tracking, and compliance. |
| Amazon Keyspaces                        | Fully managed Cassandra-compatible database service. Offers scalability, high availability, and managed infrastructure.                                                                                                                                                    |
| Amazon Timestream                       | Fully managed time series database service for collecting, storing, and processing time-series data at scale.                                                                                                                                                              |
| Amazon ElastiCache                      | Fully managed in-memory caching service supporting popular engines like Redis and Memcached.                                                                                                                                                                               |
| Amazon EMR                              | Fully managed big data platform for processing and analyzing large datasets using distributed computing frameworks such as Apache Hadoop, Apache Spark, Apache HBase, Apache Flink, Apache Hudi, and Presto.                                                               |
| Amazon QuickSight                       | Fully managed business intelligence (BI) service for creating and publishing interactive dashboards, performing ad-hoc analysis, and gaining insights from data. Suitable for data visualization, reporting, and analytics across various industries and use cases.        |
| AWS Glue                                | Fully managed extract, transform, and load (ETL) service for preparing and transforming data for analytics.                                                                                                                                                                |
| AWS Lake Formation                      | Fully managed service for building, securing, and managing data lakes on AWS.                                                                                                                                                                                              |
| Amazon Database Migration Service       | Fully managed service for migrating databases to AWS quickly and securely. Supports heterogeneous database migrations.                                                                                                                                                     |
| Amazon DMS (Database Migration Service) | Fully managed service for migrating databases to AWS quickly and securely. Supports homogeneous and heterogeneous migrations.                                                                                                                                              |



## AWS - Application Load Balancers vs API Gateway

| Feature                          | Application Load Balancer (ALB)                                                     | Amazon API Gateway                                                                               |
|----------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Layer of Load Balancing          | Layer 7 (HTTP/HTTPS)                                                                | Layer 7 (HTTP/HTTPS)                                                                             |
| Distribution of Incoming Traffic | Automatically distributes incoming traffic to backend targets                       | Exposes HTTP/HTTPS endpoints for invoking backend services and APIs                              |
| Web Application Firewall (WAF)   | Supports WAF protection out of the box                                              | Not directly supported, but can be implemented using AWS WAF                                     |
| Response Caching                 | Does not cache responses                                                            | Supports response caching                                                                        |
| Rate Limiting and Bursting       | Does not provide rate limiting or bursting capability                               | Supports rate limiting, caching, and bursting capabilities                                       |
| Static IP Availability           | Possible to get a static IP for load balancer endpoint using AWS Global Accelerator | Static IP assignment available for custom domain names through custom domain name configurations |
| Supported Protocols              | Accepts both HTTP and HTTPS traffic (SSL configuration required)                    | Accepts HTTP and HTTPS traffic (SSL configuration required)                                      |
| Request Validation and Mapping   | Cannot perform request validation or request/response mapping                       | Supports request validation, request/response mapping, and transformation                        |
| Handling Spiky Traffic           | Can handle spiky traffic with potential delay                                       | Supports burstable and auto-scaling capabilities                                                 |
| Regional Service                 | ALB is a regional service and can only integrate with Lambda in the same region     | API Gateway is a regional service but can integrate with Lambda in any region                    |
| Import/Export of Rules           | Rules cannot be imported/exported across platforms                                  | Not applicable (API configurations are managed within API Gateway)                               |
| Load Balancing Strategies        | Supports Round Robin and least connection strategies                                | Not applicable (API Gateway routes traffic based on API configurations)                          |
| Timeout Limit                    | Timeout limit is 4000 seconds                                                       | Timeout limit can be configured but typically set to 30 seconds or less                          |


## AWS batch vs Lambda
https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html


| Feature               | AWS Batch                                                                                | AWS Lambda                                                                               |
|-----------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Use Case              | Ideal for batch processing workloads, such as data ETL, machine learning, and analytics. | Suitable for event-driven, short-lived, and stateless functions triggered by events.     |
| Deployment Model      | Managed batch processing service where you define jobs, queues, and compute resources.   | Fully managed serverless compute service where you upload code and AWS handles the rest. |
| Compute Resources     | Uses managed compute environments (e.g., EC2 instances) to execute batch jobs.           | Does not require provisioning or managing compute resources; AWS handles scaling.        |
| Scaling               | Automatically scales compute resources based on workload and job requirements.           | Automatically scales based on incoming requests or events.                               |
| Execution Time Limit  | Limited only by the maximum job duration set in the job definition (up to 14 days).      | Limited to a maximum execution time of 15 minutes per invocation.                        |
| Supported Languages   | Supports various programming languages and frameworks through custom Docker images.      | Supports multiple programming languages (e.g., Node.js, Python, Java, Go, etc.).         |
| Integration           | Integrates with other AWS services such as S3, EC2, DynamoDB, and AWS Lambda.            | Can be triggered by various AWS services, including S3, SNS, DynamoDB, and more.         |
| Billing Model         | Pay-as-you-go pricing based on the resources consumed (compute resources and storage).   | Pay-as-you-go pricing based on the number of requests and compute time.                  |
| State Management      | Supports job queues and job definitions for managing job scheduling and execution.       | Stateless service; does not manage state between function invocations.                   |
| Cold Start Latency    | May experience longer startup times (cold starts) if no compute environment is running.  | May experience cold starts, but AWS continuously optimizes performance over time.        |
| Monitoring & Logging  | Provides monitoring and logging through AWS CloudWatch for job status and metrics.       | Provides monitoring and logging through AWS CloudWatch for function invocations.         |
| Environment Variables | Supports passing environment variables to job containers through job definitions.        | Supports environment variables for configuring function behavior and settings.           |


### What is Amazon Lightsail? 
  Amazon Lightsail is a virtual private server (VPS) provider and is the easiest way to get started with AWS for developers, small businesses, students, and other users who need a solution to build and host their applications on cloud.

  
