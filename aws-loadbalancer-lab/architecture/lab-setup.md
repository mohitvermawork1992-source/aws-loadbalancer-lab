\# AWS Load Balancer Lab



\## Architecture

Internet → Application Load Balancer (ALB) → EC2 Instances

Also includes Network Load Balancer (NLB) for TCP traffic.



\## Steps

1\. Created 5 EC2 instances
**AWS Services Used:**
- **5 EC2 Instances**
  - **Blue Team:** 3 EC2 instances
  - **Red Team:** 2 EC2 instances


2\. Created Application Load Balancer (public)
- Listener: Port **80 (HTTP)**
  - **Target Group 1:** Blue Team (Default routing)
  - **Target Group 2:** Red Team (Path-based routing `/test`)
  - **DNS Example:**
    - `http://ALB-1866666599.ap-south-1.elb.amazonaws.com` → Blue Team
    - `http://ALB-1866666599.ap-south-1.elb.amazonaws.com/test/` → Red Team


3\. Created Network Load Balancer (internal)
 - Created separately for testing and learning purposes
  - Used to understand Layer 4 (TCP/UDP) load balancing behavior


4\. Configured Security Groups:

&nbsp;  - ALB open on 80 to Internet

&nbsp;  - EC2 open on 80 only from ALB

5\. Tested:

&nbsp;  - ALB DNS works in browser

&nbsp;  - EC2 blocked from direct Internet

&nbsp;  - NLB tested using nc command



\## Test Result

✅ ALB HTTP works  

✅ Security group rules applied successfully  

✅ NLB TCP check passed

## 🧰 Tools Used
- **AWS Console**
- **EC2 (Amazone Linux/ Ubuntu)**
- **Load Balancers (ALB + NLB)**
- **Security Groups**
- **Browser / Curl for testing**




