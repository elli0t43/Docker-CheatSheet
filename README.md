# Installation in Arch based OS
```bash
sudo pacman -Syu
sudo pacman -S docker
```
Start the docker.service, and Auto Enable docker.service on each reboot.
```bash
sudo systemctl start docker.service
sudo systemctl enable docker.service
```

# Docker Basic Commands CheatSheet

1. Check for Docker version
```bash
sudo docker version
```
2. Check for Docker info 
```bash
sudo docker info
```
3. Check for running containers
```bash
sudo docker ps
```
4. Check for previously ran containers
```bash
sudo docker ps -a 
```
5. To run an image
```bash
sudo docker run <image-name>
```
6. Stopping a container
```bash
sudo docker stop <container-id/name>
```
7. Remove a container permanently
```bash
sudo docker rm <container-id/name>
```
> ProTip: you can simply provide the first few strings of the container id, but make sure its different than anyother docker container id. Example - `sudo docker run a30dad`
8. List all images 
```bash
sudo docker images
```
9. Delete image (Make sure you stopped all your dependent conatainers before deleting the specific image)
```bash
sudo rmi <image-name>
```
10. Pull images without running them
```bash
sudo docker pull <image-name>
```
11. Add processes to images
```bash
sudo docker run <image-name> <process>
```
example - `sudo docker run ubuntu sleep 5`
12. Execute a command in the docker container
```bash
sudo docker exec <container-id/name> <command>
```
example - `sudo docker exec brave_leakey ls -al`
13. Run docker in attach mode
```bash
sudo docker run <dockerfile>
```
14. Run docker in detach mode
```bash
sudo docker run -d <dockerfile>
```
