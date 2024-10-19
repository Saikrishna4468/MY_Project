# Automating Jenkins Installation and Web Hosting with Ansible

This project focuses on automating the installation of Jenkins and hosting a static website using **Ansible** across AWS instances. The setup involves a **master node** controlling three **managed nodes**, with tasks distributed to install Jenkins and host a static website.

## Project Overview

### Prerequisites
- AWS Account with EC2 instances.
- Ansible installed on the master node.
- Basic knowledge of YAML, SSH, and Ansible playbooks.

## Architecture
![Fig 1: Launching AWS Instances](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/AWS_ins.jpg)
### Fig 1: Launching AWS Instances
Started by launching 4 AWS instances, where I configured 1 as a **master node** and 3 as **managed nodes** to control the infrastructure effectively.

---

![Fig 2: Installing Ansible](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/ins_ansible.jpg)
### Fig 2: Installing Ansible on the Master Node
Installed **Ansible** on the master node to manage and automate the setup across the managed nodes.

---

![Fig 3: Generating SSH Key](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/gene_sshKey.jpg)
### Fig 3: Generating SSH Key for Node Connectivity
To ensure seamless communication between the master and managed nodes, I generated an **SSH key** on the master node and configured it for password-less access to the managed nodes.

---

![Fig 4: Writing Ansible Playbook](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/write_yaml.jpg)
### Fig 4: Writing an Ansible Playbook
Created a **YAML playbook** to:
- Install **Jenkins** on two of the managed nodes.
- Host a **static website** on the third node using HTML and CSS.

---

![Fig 5: Jenkins Status Before Playbook](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/jen_bef_exe.jpg)
### Fig 5: Jenkins Status Before Playbook Execution
Before running the playbook, the Jenkins service was missing on the two nodes. The system showed: **"jenkins.service could not be found."**

---

![Fig 6: Running the Playbook](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/run_yamlfile.jpg)
### Fig 6: Running the Playbook
Executed the playbook using the command `ansible-playbook -i first_playbook.yml`, which automated the following:
- Updating apt cache.
- Installing **Nginx** for web hosting.
- Installing **Jenkins** on the managed nodes.

---

![Fig 7: Jenkins Status After Playbook](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/jen_aft_exe.jpg)
### Fig 7: Jenkins Status After Playbook Execution
After running the playbook, Jenkins was successfully installed and enabled on both managed nodes. The service status changed to: **"jenkins.service enabled."**

---

![Fig 8: Static Website Hosted](https://github.com/Saikrishna4468/MY_Project/blob/main/Configuration_Management_with_Ansible/imges/website_host.jpg)
### Fig 8: Static Website Hosted
Finally, hosted a **static website** using **HTML** and **CSS** on the third managed node. The website was successfully accessible through the browser.

---

## Conclusion
This project provided hands-on experience with **Ansible** for configuration management and automation. It demonstrates how to:
- Use **Ansible** for automating complex setups across multiple nodes.
- Manage Jenkins installations and host websites using **Infrastructure as Code** principles.

### Tags
`#DevOps` `#Ansible` `#Jenkins` `#WebHosting` `#CloudComputing` `#AWS` `#Automation` `#InfrastructureAsCode` `#CI/CD` `#TechJourney` `#LearningInPublic`
