# Splunk Enterprise Ansible Role

Ansible role to **install and configure Splunk Enterprise components** in a distributed environment, including Search Heads (SH), Indexers (IDX), Heavy Forwarders (HF), License Manager (LM) Cluster Manager (CM) Search Head Cluster Deployer (SHCD) Deployement Server (DS).  

This role is designed for **offline servers** where internet access is not available.  
All sensitive variables, including passwords and secrets, can be securely managed using **Ansible Vault**.  

The role allows you to place the **latest Splunk version** in a specified directory, which is configurable via role variables, so installation is flexible and controlled.

---

## **Features**

- Install Splunk Enterprise on **RedHat, CentOS, Oracle Linux, and Ubuntu**.
- Configure **All of Components**.
- Handles **service restarts and port availability**.
- Designed for **distributed Splunk environments**.
- Easy to include in your playbooks and scale to multiple hosts.

---

## **Requirements**

- Ansible **2.9+**
- Sudo privileges on target hosts
- Supported platforms:
  - Ubuntu 
  - RedHat/Oracle Linux 

---
