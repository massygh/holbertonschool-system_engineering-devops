# Web Infrastructure Design Project

## General Information

This project involves designing and documenting different web infrastructure setups. The goal is to provide a clear, scalable, and secure architecture for hosting a website, ensuring all components are well-understood and explained.

### Key Instructions

1. **Design and Whiteboarding**: For each task, design the infrastructure on a whiteboard or software, then take a picture/screenshot of your diagram.
2. **Screenshots and Links**: Upload screenshots to an image hosting service (e.g., Imgur) and insert the links into the answer file. Push the answer file to GitHub and provide the GitHub file link where required.
3. **Whiteboarding Session**: Each task must be explained in front of a mentor, staff, or student without using a computer or notes.
4. **Requirements**: Focus on answering what is asked in the requirements. Avoid being too verbose and only cover necessary details.

## Tasks

### 0. Simple Web Stack

Design a simple web infrastructure with the following components:
- 1 server
- 1 web server (Nginx)
- 1 application server
- 1 application files (code base)
- 1 database (MySQL)
- 1 domain name `foobar.com` configured with a `www` record pointing to IP `8.8.8.8`

**Explanation Points**:
- What is a server
- Role of the domain name and type of DNS record
- Role of the web server, application server, and database
- Communication between server and user computer
- Issues: SPOF, downtime during maintenance, scalability concerns

**File**: `0-simple_web_stack`

### 1. Distributed Web Infrastructure

Design a distributed web infrastructure with the following components:
- 2 servers
- 1 web server (Nginx)
- 1 application server
- 1 load-balancer (HAproxy)
- 1 set of application files (code base)
- 1 database (MySQL)

**Explanation Points**:
- Justification for each additional element
- Load balancer distribution algorithm and setup (Active-Active vs Active-Passive)
- Primary-Replica (Master-Slave) database cluster
- Differences between Primary and Replica nodes

**Issues**:
- SPOF locations
- Security issues (no firewall, no HTTPS)
- Lack of monitoring

**File**: `1-distributed_web_infrastructure`

### 2. Secured and Monitored Web Infrastructure

Design a secured and monitored web infrastructure with:
- 3 firewalls
- 1 SSL certificate for HTTPS
- 3 monitoring clients (e.g., Sumologic)

**Explanation Points**:
- Purpose of each additional element
- Role of firewalls
- Importance of HTTPS
- Monitoring and data collection methods
- Monitoring web server QPS

**Issues**:
- SSL termination at load balancer level
- Single MySQL server for writes
- Identical components across servers

**File**: `2-secured_and_monitored_web_infrastructure`

### 3. Scale Up

Design a scalable infrastructure with:
- 1 additional server
- 1 load-balancer (HAproxy) configured as a cluster with the existing one
- Separation of components (web server, application server, database) onto separate servers

**Explanation Points**:
- Justification for additional elements

**File**: `3-scale_up`

## Repository Details

- **GitHub Repository**: [holbertonschool-system_engineering-devops](https://github.com/holbertonschool/system_engineering-devops)
- **Directory**: `web_infrastructure_design`
