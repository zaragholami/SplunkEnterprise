# Splunk Enterprise Ansible Role

Ansible role to **install and configure Splunk Enterprise components** in a distributed environment, including Search Heads (SH), Indexers (IDX), Heavy Forwarders (HF), and License Manager (LM).  

This role handles installation, configuration, service restarts, and ensures ports are ready before continuing tasks.

---

## **Features**

- Install Splunk Enterprise on **RedHat, CentOS, Oracle Linux, and Ubuntu**.
- Configure **Search Heads, Indexers, Heavy Forwarders, License Manager**.
- Handles **service restarts and port availability**.
- Designed for **distributed Splunk environments**.
- Easy to include in your playbooks and scale to multiple hosts.

---

## **Requirements**

- Ansible **2.9+**
- Sudo privileges on target hosts
- Supported platforms:
  - Ubuntu (all supported versions)
  - RedHat/CentOS/Oracle Linux 7, 8

---

## **Example Playbook**

```yaml
- hosts: sh
  become: yes
  roles:
    - splunk
