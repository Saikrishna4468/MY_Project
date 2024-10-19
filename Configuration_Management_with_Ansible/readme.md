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

![Fig 2: Installing Ansible](path/to/fig2.png)
### Fig 2: Installing Ansible on the Master Node
Installed **Ansible** on the master node to manage and automate the setup across the managed nodes.

---

![Fig 3: Generating SSH Key](path/to/fig3.png)
### Fig 3: Generating SSH Key for Node Connectivity
To ensure seamless communication between the master and managed nodes, I generated an **SSH key** on the master node and configured it for password-less access to the managed nodes.

---

![Fig 4: Writing Ansible Playbook](path/to/fig4.png)
### Fig 4: Writing an Ansible Playbook
Created a **YAML playbook** to:
- Install **Jenkins** on two of the managed nodes.
- Host a **static website** on the third node using HTML and CSS.

---

![Fig 5: Jenkins Status Before Playbook](path/to/fig5.png)
### Fig 5: Jenkins Status Before Playbook Execution
Before running the playbook, the Jenkins service was missing on the two nodes. The system showed: **"jenkins.service could not be found."**

---

![Fig 6: Running the Playbook](path/to/fig6.png)
### Fig 6: Running the Playbook
Executed the playbook using the command `ansible-playbook -i first_playbook.yml`, which automated the following:
- Updating apt cache.
- Installing **Nginx** for web hosting.
- Installing **Jenkins** on the managed nodes.

---

![Fig 7: Jenkins Status After Playbook](path/to/fig7.png)
### Fig 7: Jenkins Status After Playbook Execution
After running the playbook, Jenkins was successfully installed and enabled on both managed nodes. The service status changed to: **"jenkins.service enabled."**

---

![Fig 8: Static Website Hosted](path/to/fig8.png)
### Fig 8: Static Website Hosted
Finally, hosted a **static website** using **HTML** and **CSS** on the third managed node. The website was successfully accessible through the browser.

---

## Conclusion
This project provided hands-on experience with **Ansible** for configuration management and automation. It demonstrates how to:
- Use **Ansible** for automating complex setups across multiple nodes.
- Manage Jenkins installations and host websites using **Infrastructure as Code** principles.

Feel free to explore, clone, or contribute to this project!

## Connect with Me
If you found this project interesting or have any suggestions, let's connect on [LinkedIn](https://www.linkedin.com) and share ideas.

---

### Tags
`#DevOps` `#Ansible` `#Jenkins` `#WebHosting` `#CloudComputing` `#AWS` `#Automation` `#InfrastructureAsCode` `#CI/CD` `#TechJourney` `#LearningInPublic`

---

Replace `path/to/figX.png` with the actual paths to your images. If the images are hosted online, use their URLs instead. This `README.md` file should be easy to understand and provide a detailed overview of your project for anyone visiting your GitHub repository.
