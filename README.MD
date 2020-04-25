# docker-cheat-sheet
Quick reference guide for Docker commands - not at all exhaustive, just a cheat sheet.

## Installing Docker

| task | command |
|:-----|:--------|
| get image | `wget -qO- https://get.docker.com/ | sh`|  
| Check version | `docker --version` |  
| Add user to docker group | `sudo usermod -aG docker $(whoami)`|  
| commit change | `ctrl + d` | 

## Installing Docker

| task | command |
|:-----|:--------|
| Donload stable release | `sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`|  
| Apply executable permissions to the binary | `sudo chmod +x /usr/local/bin/docker-compose` |  
| create a symbolic link to /usr/bin or any other directory in your path | `sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose`|  
| Test the installation | `docker-compose --version` | 



## Running a Container

| task | command |
|:-----|:--------|
| Make new directory    |  `mkdir -p ~/html`     |
| Expose external port and run nginx | `docker run --name nginx -p 9091:80 -d -v ~/html:/usr/share/nginx/html nginx:1.17` |
| report a snapshot of the current processes | `docker ps -a` |
