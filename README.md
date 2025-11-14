# Splunk Enterprise Ansible Role

Ansible role to **install and configure Splunk Enterprise components** in a distributed environment, including Search Heads (SH), Indexers (IDX), Heavy Forwarders (HF), License Manager (LM) Cluster Manager (CM) Search Head Cluster Deployer (SHCD) Deployement Server (DS).  

This role handles installation, configuration, service restarts, and ensures ports are ready before continuing tasks.

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

## **Example Playbook**

```yaml
- hosts: sh
  become: yes
  roles:
    - splunk
