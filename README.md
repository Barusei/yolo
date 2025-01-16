# Overview
This project involved the virtualization and deployment of a full-stack yolo application 
Ensure the following tools are installed -vagrant, virtualbox, ansible and git & github
Clone the Repository
# Start the Virtual Machine
vagrant init ubuntu/trusty64
#run virtual box
Use vagrant up --provison command
vagrant reload --to reload virtualbox after changes e.g in specs
vagrant ssh --to ssh into the virualbox
# Run Ansible Playbook
ansible-playbook -i ansible/inventory/hosts.ini ansible/playbook.yml

# Run Docker Compose
docker-compose up --build
# Configuration Files
  inventory File (ansible/inventory/hosts.ini)
  # Defines the target hosts for Ansible.
  Playbook File 
  # Defines tasks for setting up and deploying the application.
