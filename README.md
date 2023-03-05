## Test Environment for Ansible 
- controller: ansible controll node
- hostX: ansible managed node(s)

**Prerequirements**

- ssh/ssh_private
- ssh/ssh_public

**Container management**
- Start: docker-compose.exe up --build -d
- Stop: <br> docker-compose.exe down
- Connect to: <br> docker exec -it \<CONTAINER> bash

**Todo**
- Build a key generator to automate the process





