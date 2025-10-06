# aws-loadbalancer-lab
Hands-on AWS Lab: Internet → Application Load Balancer → EC2 + Testing with Security Groups
**AWS Services Used:**
- **5 EC2 Instances**
  - **Blue Team:** 3 EC2 instances
  - **Red Team:** 2 EC2 instances
- **1 Application Load Balancer (ALB)**
  - Listener: Port **80 (HTTP)**
  - **Target Group 1:** Blue Team (Default routing)
  - **Target Group 2:** Red Team (Path-based routing `/test`)
  - **DNS Example:**
    - `http://ALB-1866666599.ap-south-1.elb.amazonaws.com` → Blue Team
    - `http://ALB-1866666599.ap-south-1.elb.amazonaws.com/test/` → Red Team
- **1 Network Load Balancer (NLB)**
  - Created separately for testing and learning purposes
  - Used to understand Layer 4 (TCP/UDP) load balancing behavior
    
## 🧰 Tools Used
- **AWS Console**
- **EC2 (Amazon Linux / Ubuntu)**
- **Load Balancers (ALB + NLB)**
- **Security Groups**
- **Browser / Curl for testing**
