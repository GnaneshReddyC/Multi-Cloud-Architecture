company: CODTECH IT SOLUTION

NAME:GNANESH REDDY C

INTER ID:CTIS5317

DOMAIN: CLOUD COMPUTING

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

Design and Implementation of a Simulated Multi-Cloud Architecture Using AWS

This project demonstrates the design and implementation of a simulated multi-cloud architecture using services within Amazon Web Services (AWS). Although deployed within a single cloud provider, the architecture follows multi-cloud principles by creating two logically isolated environments that function as independent cloud domains. Services are distributed across these isolated environments and integrated through secure HTTP-based communication, thereby demonstrating interoperability between platforms.

The architecture consists of two separate Virtual Private Clouds (VPCs) within AWS. The first environment, referred to as Cloud A (Frontend Environment), hosts a web server configured using Nginx. The second environment, referred to as Cloud B (Backend Environment), hosts a REST API developed using the Flask framework. Each VPC has its own CIDR block, subnet configuration, route tables, and internet gateway, ensuring complete logical separation. This isolation simulates two independent cloud providers communicating across a network boundary.

VPC-A was created with a CIDR block of 10.0.0.0/16 and contains a public subnet (10.0.1.0/24). An Internet Gateway was attached to allow inbound and outbound internet traffic. A route table was configured to route 0.0.0.0/0 traffic to the Internet Gateway. Within this VPC, an EC2 instance running Amazon Linux 2 was launched to serve as the frontend web server. Nginx was installed and configured to act as a reverse proxy server. The security group attached to this instance allows inbound HTTP (port 80) and SSH (port 22) access.

VPC-B was created separately with a CIDR block of 192.168.0.0/16 and a public subnet (192.168.1.0/24). Similar networking components were configured, including an Internet Gateway and route table. An EC2 instance was launched inside this VPC to function as the backend server. Python 3 and Flask were installed on this instance, and a simple API endpoint was created to return a JSON response when accessed at /api. The backend security group was configured to allow inbound traffic on port 5000 for API communication, along with SSH access for administration.

The interoperability between the two simulated cloud environments was achieved by configuring Nginx in the frontend server to forward incoming API requests to the backend server’s public IP address. When a user accesses the frontend server through a web browser and navigates to /api, the request is proxied to the backend server hosted in the separate VPC. The backend processes the request and returns a JSON response, which is then displayed to the user via the frontend interface.

The final output of the system is a JSON message such as:

{"message":"Response from Simulated Cloud B (VPC-B)"}

This confirms that the frontend service deployed in one isolated environment successfully communicates with the backend service deployed in another isolated environment. The demonstration clearly shows distributed service deployment and cross-environment integration, which are core principles of multi-cloud architecture.

This architecture offers several advantages. First, it demonstrates service isolation and modular design. Each environment can be managed, scaled, or modified independently without affecting the other. Second, it reflects real-world enterprise architecture patterns where frontend and backend services are separated across different network domains. Third, it improves security posture by limiting direct exposure of backend services. Finally, the design promotes scalability and fault isolation.

In conclusion, this project successfully simulates a multi-cloud architecture using two independent VPC environments within AWS. By distributing services across separate networking domains and enabling controlled interoperability through HTTP-based communication, the implementation satisfies the requirement of designing a multi-cloud architecture and demonstrating platform interoperability. The architecture effectively models how services would communicate across different cloud providers in a production environment while maintaining simplicity and clarity for demonstration purposes.
