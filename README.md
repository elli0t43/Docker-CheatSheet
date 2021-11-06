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
> Pro Tip: you can simply provide the first few strings of the container id, but make sure its different than anyother docker container id. Example - `sudo docker run a30dad`
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

# Intermediate Commands CheatSheet 

### Run command
1. To run a specific image version
```bash
sudo docker run <image-name>:<version>
```
Example - `sudo docker run redis:4.0`
2. To run the docker file in interactive mode
```bash
sudo docker run -i <docker-file>
```
3. To run the docker file in interactive with terminal mode
```bash
sudo docker run -it <docker-fil>
```
4. To port map a docker container
```bash
sudo docker run -p <new-port-number>:<old-port-number> <docker-file>
```
5. To volume map inside a docker container
```bash
sudo docker run -v /opt/datedir:/var/lib/mysql mysql
```
6. Inspect Container
```bash
sudo docker inspect <container-id/name>
```
7. Container logs
```bash
sudo docker logs <container-id/name>
```
8. Set an Env variable inside docker
```bash
sudo docker run -e <env variable> <container-id/name>
```
### Build Command
1. Building a docker image (This image will only be available to local only)
```bash
sudo docker build <dockerfile> -t <docker-image-name>
```
example
```bash
sudo docker build dockerfile -t elli0t43/test-dockerimage
```
>Pro Tip: Dockerfile uses a specific indentation or Instruction and Argument format, The uppercase words like `RUN`,`FROM`,`COPY` etc are Instruction, and generally written in uppercase, after that their is Argument, Which is generally some commands that needs to be ran, or be excuted with their Instruction, like `sudo apt update`, `apt-get install python`.
2. Push your docker image,(By pushing your image will available to others)
```bash
sudo docker push <docker-image-name>
```



