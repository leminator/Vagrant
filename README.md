# Vagrant Technical Exercise
#Envrionment:
  #Python 3.9 
  #Ansible [core 2.12.2]
  #Vagrant 2.2.19
  #Nginx Docker 20.10.12
  #Virtual Box w/ CentOS 7 
  #MacOSX / Linux native OS
  
  Create the envrionment using the tools indicated 
  
  Create a directory to store the Vagrant file, playbooks (.yml), and VM Logs (i.e. Inventory)
  
  In the etc directory, copy/create the ansible config file indicated to set python 3.9 as the interpreting language. (To avoid hours of "why are there so many          versions of python on my system and none of them are speaking to ansible headaches".)
      https://docs.ansible.com/ansible/latest/reference_appendices/interpreter_discovery.html
      
  In order for Ansible to be able to deploy containers you’ll also need to install the following Python module using the same version of Python that Ansible is           pointing towards:
        pip3 install docker
        
  Once the directories, tools and services are established:
          > cd /file/path/to/inventory
          > vagrant up (will pull instructions from the vagrantfile to execute the playbooks)
          
          ... vm starts auto provisioning ...
          
          Virtual box is now accessibe via virtualbox cmd
            Upon accesing, will be prompted for user credentials
          Docker is now running a local nginx image on port 8080
            Going into your browser: http://localhost:8080/ indicates the server is alive
  
 ** Working issue: Using python, passlib has to be incorporated in order to create SHA based encrytion for passwords. 
    https://docs.ansible.com/ansible/latest/reference_appendices/faq.html
    
  
