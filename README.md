# Overview
This project involved the virtualization and deployment of a full-stack yolo application project
Ensure the following tools are installed -vagrant, virtualbox, ansible and git & github
Clone the Repository--git clone https://github.com/Barusei/yolo
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


# container orchestration
  container orchestration tool used in this project is kubernetes 
  deployment.yaml used for setting of replicaset and the number of pod replicas to be created 
  service.yaml is used in managing connection to the pods using clusterIP, service IPs and even controls load balancing to the pods
  
