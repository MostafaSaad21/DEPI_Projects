Deploy Flask Notes App on AWS EC2 with Ansible

# 1. Environment Setup on AWS EC2 (Amazon Linux)
- Launch an EC2 instance with Amazon Linux AMI (similar to RHEL).
- Choose instance type (e.g., t2.micro for testing).
- Configure Security Group to allow inbound ports:
  - SSH (port 22) from your IP.
  - HTTP (port 5000) from anywhere (0.0.0.0/0) or your IP for testing.
- Generate or use existing SSH key pair for access.
<img width="1896" height="523" alt="image_1" src="https://github.com/user-attachments/assets/a64b8c29-bf01-43f2-ae11-7d6ce020515f" />



2. Ansible Controller and Inventory Setup
- On your local machine or a separate server, install Ansible.
- Create an host file (e.g., inventory) with content:



<img width="900" height="133" alt="image" src="https://github.com/user-attachments/assets/0deb9c7d-acc2-46c7-8acf-ed4800acce77" />





3. Create Ansible Playbook and Role for Deployment

<img width="380" height="464" alt="image" src="https://github.com/user-attachments/assets/86d625eb-d50c-4941-9dc8-aa479451ea33" />


# 4 Running the Application with VS code :
- Connect to EC2 instance:
-  Test connection with host :
  
  <img width="900" height="148" alt="image" src="https://github.com/user-attachments/assets/0f9b496b-854b-4f10-8b5f-7aadbc82d648" />


# 6. Configure Security Group
- Make sure inbound rules allow port 5000 (TCP) from your IP or anywhere for testing.
- This allows browser access to Flask server running on port 5000.

  <img width="900" height="384" alt="image" src="https://github.com/user-attachments/assets/9cbf60ab-59a9-4869-aebc-1d30cbb7ff94" />


7. Run the playbook :


<img width="900" height="627" alt="image" src="https://github.com/user-attachments/assets/00f12495-83ca-4963-a546-217017c0def1" />



8 Running the Application:

<img width="900" height="548" alt="image" src="https://github.com/user-attachments/assets/23b5f832-772d-4747-87f9-0bcf44d6168c" />


9. Verifying Data in SQLite Database

<img width="746" height="231" alt="image" src="https://github.com/user-attachments/assets/4714de22-e5c0-468c-8ccc-d3a0e5208c37" />



