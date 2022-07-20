### Peter Blattman-White -- ELK Stack Project

Automated ELK Stack Deployment
==============================

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the YML file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

  - [Ansible Hosts](ansible/hosts.yml)
  - [Metricbeat Playbook](ansible/roles/metricbeat-playbook.yml)
  - [Filebeat Playbook](ansible/roles/filebeat-playbook.yml)
  - [Ansible Configuration](ansible/ansible.cfg)
  - [Metricbeat Configuration File](ansible/files/metricbeat-config.yml)
  - [Filebeat Configuration File](ansible/files/filebeat-config.yml)
  - [ELK Playbook](ansible/elkserversetup.yml)
  - [Pen Test Playbook (DVWA Containers)](ansible/pentest.yml)

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting traffic to the network.
- _What aspect of security do load balancers protect? What is the advantage of a jump box?_
  - Load balancers help ensure complete environment functionality and availability/accessibility, through the distribution of incoming data to several web servers.
  - Jump boxes allow for simplified administration of multiple systems and provide an additional layer between the outside and internal assets.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the network and system logs.
- _What does Filebeat watch for?_
  - Filebeat monitors the log files or any any other items/locations that you specify, collects log events, and forwards these logs to the ELK Server.
- _What does Metricbeat record?_
  - Metricbeat takes the metrics and statistics that it collects (for example, system metrics including CPU and disk usage, overall memory usage etc) and forwards this information to the Elk Server for review and further analysis.

The configuration details of each machine may be found below.

|    Name     |      Function      | IP Address | Operating System |
|-------------|--------------------|------------|------------------|
| Jump Box    | Gateway & Ansible  | 10.0.0.7   | Linux            |
| Web-1       | Ubuntu Web Server  | 10.0.0.11  | Linux            |
| Web-2       | Ubuntu Web Server  | 10.0.0.10  | Linux            |
| ELK-Server  | Base for ELK Stack | 10.0.0.5   | Linux            |

-------------------------------------------------------------------------------------------------------------------------------------------

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box Provisioner machine can accept connections from the Internet.
Access to this machine is only allowed from the following IP addresses:
- Personal IP Address

Machines within the network can only be accessed by the Jump Box Provisioner.
- _Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

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