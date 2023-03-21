# Ansible-Sample-Application-Deployment
This repository will contain sample code to deploy the sample application on linux instance




# Directory Structure
  1. configs - contain environment specific variable
  2. inventories - contains inventory file for each environment
  3. groups_vars - contains common variables across environments
  4. roles - This will have subfolders like java,tomcat

        a) add_devops_user - This folder will have files related to the setup of initial user

  5. main.yml - This is the main file which will execute roles in the playbook


# How to Run the Playbook



```
ansible-playbook main.yml -i inventories/dev/hosts --user ec2-user --key-file /home/ec2-user/playbooks/ansible_auth.pem -e '@configs/dev.yml'

ansible-playbook main.yml -i inventories/dev/hosts --user devops --key-file /home/devops/.ssh/id_rsa -e '@configs/dev.yml'


```
# References


