# Task-1: Writing CI/CD Deployment Task Using GitHub Runner
## 1. Setting up server (Writing a bash script)
### a. Setting up docker on a linux machine
- Created a file named *docker_install.sh*
- Written following commands to the file
<pre> # Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
</pre>
- Made the file executable
<pre>chmod +x docker_install.sh</pre>
- Ran the the following command to install the docker
<pre>./docker_install.sh</pre>
- Installed the docker packages using following
<pre>sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin</pre>
- Now the docker has been successfully installed in our linux machine
- We can check the docker availability
<pre>
docker --vesion
docker run hello-world
</pre>
![Successful Docker Installation](./images/succesful_docker_install.png)

### c. Installing Nginx
- Installed Nginx server using following commands
<pre>
sudo apt update
sudo install nginx
</pre>
- Successful installation of nginx
![Web View](./images/active_wed.png)</br>
- Terminal view
![Terminal View](./images/actice_server_demo.png)



