# Elk_Project
Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](/Onedrive/Documents/NetworkDiagram.Drawio)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: my-playbook2.yml_

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly secure, in addition to restricting access to the network.
- _TODO: The Load Balancer is a device that acts as a reverse proxy and distributes network or application traffic across a number of servers. Load balancers are used to increase capacity (concurrent users) and reliability of applications and helps defend against DDOS attacks.
The Jump server acts as a single gateway for auditing authentication as well as monitoring users.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the __Data___ and system _logs____.
- _TODO: What does Filebeat watch for?_Filebeat is a lightweight shipper for forwarding and centralizing log data
- _TODO: What does Metricbeat record?_Metricbeat collects metrics and statistics to the output you specify such as Elasticsearch

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux            |
| web-1    | web host | 10.0.0.5   | Linux            |
| Web-2    | web host |  10.0.0.8  | Linux            |
| ELK_VM   | Monitoring|  10.1.0.4  | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the __ELK-VM___ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: 207.135.249.159_

Machines within the network can only be accessed by _Jump Box____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | No                  | 10.0.0.5 10.0.0.8 10.1.0.4   |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_The main benefit to automating configuration with ansible is the ability to configure multiple machines at once.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._Install Docker	
- ...Install Python
- ...Increase Virtual Memory

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Onedrive/Pictures/Elk-VMconfig.jpeg)  

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_
10.0.0.8 10.0.07

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_
Filebeat and metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._
Filebeat Collects log events such as usage patterns, activites, and operations within a server or another device.
Metricbeat takes metrics and statistics such as system-level CPU usage, memory, file system, disk IO, and network IO statistics 

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
