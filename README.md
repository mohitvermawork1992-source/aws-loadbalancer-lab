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
- **EC2 (Ubuntu)**
- **Load Balancers (ALB + NLB)**
- **Security Groups**
- **Browser / Curl for testing**

## 🧠 Learning Outcomes
✅ Understood how ALB distributes traffic between multiple target groups  
✅ Learned how **path-based routing** works (`/test` → different target group)  
✅ Practiced **security group rules** and **connectivity testing**  
✅ Gained initial knowledge about **Network Load Balancer (NLB)** setup
