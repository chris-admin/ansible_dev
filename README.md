## Test Environment for Ansible 
- **controller:** ansible controll node
- **hostX:** ansible managed node(s)

### Prerequirements
- ssh/ssh_private
- ssh/ssh_public

### Container management
- **Start:** <br> docker-compose.exe up --build -d
- **Stop:** <br> docker-compose.exe down
- **Connect to:** <br> docker exec -it \<CONTAINER> bash

### docker-compose.yml
**dockerfile** is a way to modify the container OS (e.g. yum install, edit some config files etc.) The Host container will run **SSHD** via **CMD** so the container will not shut down immediately. The **controller-node** need the option **tty: true** otherwise the container will stop after the booting process. **ansible.cfg** musst be locaded in a directory not accessable by other users so you have to change the permissions of the volume **./ansible:/ansible:0770**.

### Todo
- Build a key generator to automate the process
