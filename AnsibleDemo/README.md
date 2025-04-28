### Just playing aroung Ansible on AWS.

1. Launch 2 ubuntu instances. 'Ansible-Server' and target-ubuntu
2. Launch 'Ansible-Server' on your terminal
3. create 'ansible' repository and install ansible on it

# Connect to the 'target server'
1. ssh-keygen
2. ls /home/ubuntu/.ssh/ - to list the keys you just generated in the .ssh file location
3. cat /home/ubuntu/.ssh/id-rsa.pub - to view the public key. then copy
4. Launch target server on a new tab.
5. perform same process 1, 2 and 3
6. vim ~/.ssh/autorized-keys - to open the authorized keys file
7. copy the public key from first tab 'Ansible-Server tab' and paste in the vim file
8. ssh 'public ip address of target-ubuntu'

## Ansible adhoc commands
1. Create a file named 'inventory' and add the ip address of 'target-ubuntu'. Which means if i have 10 target servers i would just include them in the inventory file careated 
2. ansible -i inventory all -m "shell" -a "touch devopsclass" : This command is meant to create 'devopsclass' files in all target address whose ip address is listed in inventory.

## Playbook command
