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
5. Rrun an image
```bash
sudo docker run <image-name>
```
6. Stopping a container
```bash
sudo docker stop <container-id/name>
```
7. Remove a container permanenently
```bash
sudo docker rm <container-id/name>
```
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
12. 
