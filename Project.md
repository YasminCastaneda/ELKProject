## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_Load balancers protect against distributed DDoS attacks. The advantage of a jump box is in order to access it you need the IP address to connect to any of the servers. In order to Jump into other machines you need JumpBox.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the data and system system logs.
- _TODO: What does Filebeat watch for?_ It works with Elasticsearch that a lot of companies use to watch log files, monitoring them, etc.
- _TODO: What does Metricbeat record?_Metricbeats records the statistics and metrics.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function   | IP Addresses | Operating System |
|----------|------------|--------------|------------------|
| Jump Box | Gateway    | 10.0.0.4     | Linux            |
| ELK VM   | Monotoring | 10.1.0.4     | Linux            |
| Web 1    | Monitoring | 10.1.0.5     | Linux            |
| Web 2    | Monitoring | 10.0.0.6     | Linux            |
### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the jump box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: _ 24.20.214.230

Machines within the network can only be accessed by JumpBox.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_ The machine I allowed to access the Elk VM is my personal Machine. The IP address is  24.20.214.230

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 23.27.44.2           |
| ELK VM   | No                  | 10.1.0.4             |
| Web 1    | No                  | 10.1.0.5             |
| Web 2    | No                  | 10.0.0.6             |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_The main advantage of Ansible is being able to monitor and access different servers with 1 person instead of having to go to each one taking time. It is more efficient if you need to deploy something new.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- sudo apt install docker.io
- sudo docker images
-  

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

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