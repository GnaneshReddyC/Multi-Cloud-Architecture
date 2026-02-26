company: CODTECH IT SOLUTION

NAME:GNANESH REDDY C

INTER ID:CTIS5317

DOMAIN: CLOUD COMPUTING

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

Design and Implementation of a Simulated Multi-Cloud Architecture Using AWS

A multi-cloud architecture refers to a cloud computing strategy in which services and workloads are distributed across more than one cloud service provider. In this implementation, services are deployed across Amazon Web Services (AWS) and Microsoft Azure (Azure) to demonstrate interoperability, scalability, and resilience. The objective of this architecture is to avoid vendor lock-in, improve availability, and leverage the strengths of each provider while enabling secure communication between platforms.

The architecture is logically divided into frontend, backend, database, and storage layers, with responsibilities shared between AWS and Azure. On the AWS side, the backend application is hosted on an Elastic Compute Cloud (EC2) instance. This backend service exposes RESTful APIs over HTTPS, allowing external systems to securely communicate with it. The application server processes business logic and interacts with a managed relational database service (RDS) instance for structured data storage. AWS Identity and Access Management (IAM) roles are configured to enforce least-privilege access control, ensuring secure resource interaction within the AWS environment. Security Groups are used as virtual firewalls to restrict inbound and outbound traffic based on specific ports and IP ranges.

On the Azure side, a Virtual Machine (VM) is deployed to host the frontend application. The frontend is responsible for user interaction and communicates with the AWS backend through secure API calls. Network Security Groups (NSGs) are configured in Azure to control traffic flow and allow outbound HTTPS communication toward the AWS EC2 public endpoint. This configuration demonstrates cross-cloud communication, where an application running in Azure consumes services hosted in AWS. Additionally, Azure Blob Storage is configured to store backup files or replicated objects received from the AWS environment, thereby showcasing cross-platform storage interoperability.

Interoperability between the two cloud providers is achieved using standardized internet protocols such as HTTPS and REST APIs. Since both platforms support open networking standards, communication is established over public endpoints with encryption enabled through TLS. This ensures confidentiality and integrity of data during transmission. The Azure VM sends HTTP requests to the AWS EC2 instance’s public IP address or DNS endpoint. Upon receiving the request, the backend processes it, interacts with the RDS database if necessary, and returns a structured JSON response. This response is then rendered on the frontend hosted in Azure. Such communication validates that services running on separate cloud infrastructures can seamlessly interact without dependency on proprietary integrations.

From a data management perspective, the backend stores application data in AWS RDS, ensuring high availability and automated backups within AWS. Selected data or backup files can be transferred to Azure Blob Storage using secure upload mechanisms. This demonstrates data portability across cloud providers, which is a critical feature of multi-cloud strategies. By replicating or backing up data across providers, the architecture enhances disaster recovery capabilities and ensures business continuity in case one provider experiences downtime.

Monitoring and logging are essential components of the design. AWS monitoring services track EC2 performance metrics such as CPU utilization, network traffic, and disk usage. Similarly, Azure Monitor can be used to observe VM performance and networking metrics. These monitoring tools ensure that administrators can detect anomalies, troubleshoot issues, and maintain system health across both platforms. Although managed independently, operational visibility is maintained for each cloud environment.

Security considerations play a major role in this architecture. All API communications are encrypted using HTTPS, firewall rules are tightly controlled, and access credentials are securely managed. Public exposure is minimized by allowing only required ports such as 80 or 443 for web communication and restricting database access to internal networks. Proper role-based access control ensures that services interact securely without exposing sensitive credentials in application code.

This multi-cloud implementation demonstrates how distributed cloud services can operate cohesively while residing on separate infrastructures. The design ensures scalability by allowing independent scaling of frontend and backend components within their respective cloud environments. It improves fault tolerance by reducing dependency on a single provider. Furthermore, it prepares organizations for hybrid expansion and advanced disaster recovery planning. Overall, the architecture successfully validates interoperability between AWS and Azure while maintaining secure, scalable, and resilient cloud operations.

In conclusion, this project successfully simulates a multi-cloud architecture using two independent VPC environments within AWS. By distributing services across separate networking domains and enabling controlled interoperability through HTTP-based communication, the implementation satisfies the requirement of designing a multi-cloud architecture and demonstrating platform interoperability. The architecture effectively models how services would communicate across different cloud providers in a production environment while maintaining simplicity and clarity for demonstration purposes.


<img width="717" height="238" alt="Image" src="https://github.com/user-attachments/assets/04d13113-83bb-48af-9b3a-92820edb5907" />

<img width="1218" height="721" alt="Image" src="https://github.com/user-attachments/assets/855ef0a3-117b-4693-9551-427ffb85e1d3" />

<img width="1886" height="275" alt="Image" src="https://github.com/user-attachments/assets/0bfefa95-d844-46cf-b50a-68e8f4b537c7" />

<img width="818" height="243" alt="Image" src="https://github.com/user-attachments/assets/a46e747a-8e0b-40bf-845e-36b69b4ee864" />

<img width="1886" height="449" alt="Image" src="https://github.com/user-attachments/assets/5a90b4c5-c208-4104-8751-0090cf9dbbe7" />

<img width="1886" height="275" alt="Image" src="https://github.com/user-attachments/assets/e4badbfa-9202-4cd8-9d62-9745d49f6fb5" />
