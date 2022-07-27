# Purpose
Deploying Docker containers to AWS.

## SSH Using Windows
Download PuTTY to SSH to Windows

## After Connected To Your EC2 Instance
Refer to [THIS](https://onedigital.udemy.com/course/docker-kubernetes-the-practical-guide/learn/lecture/22626493#overview)

1. Make sure that EC2 instance has the latest version of packages
```bash
sudo yum update -y
```

2. Install Docker in EC2 Instance
```bash
sudo amazon-linux-extras install docker
```

3. Set Up A Public Docker Repo

4. `docker login` in the terminal to allow you to push

5. Run The Docker Container
```bash
   sudo docker run -d -rm -p 80:80 <name_of_docker_repo>
```

Check if it's running by `sudo docker ps`

6. Docker Image on AWS
Docker Image should also be running on the EC2 instance. The address is listed under `IPv4 Public IP`.
Modification to Security Group is needed particularly in `Inbound Rules` to allow HTTP/HTTPS ports. 
