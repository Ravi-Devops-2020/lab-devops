# lab-devops
DevOps

1.	Created basic centos VM using the following 
Installed software’s –
•	Oracle Virtual Box - Hypervisor
•	Vagrant – VM provisioner
•	Putty – To connect host machine using SSH
Ran following commands to provision VM as per the configurations mentioned in  https://github.com/Ravi-Devops-2020/lab-devops/Vagrantfile
o	Vagrant init
o	Vagrant up

2.	Installed Docker on VM created above
I.	Connected VM using Putty.
II.	Created and provided executable permission to script file with all the required commands to install the following on VM created above, also enabled docker service to start by default when server rebooted.
•	Docker repo
•	Docker-engine
•	Docker-compose
III.	Script file - https://github.com/Ravi-Devops-2020/lab-devops/Docker_Install_Script.sh

3.	Created a Jenkins instance using docker container
I.	Created and changed to “/home/jenkins/jenkins-data” directory to maintain lab data at one place.
II.	Pulled Docker image from repo using the command $ docker pull jenkins/Jenkins
III.	Created a docker-compose.yml file with all necessary configurations to spin up Jenkins service using docker container.
docker-compose.yml file - https://github.com/Ravi-Devops-2020/lab-devops/blob/development/Jenkins/docker-compose.yml
IV.	Executed the command $ docker compose up -d to run the container using the image pulled above.

4.	Access Jenkins from host machine 
I.	Checked the container status using the command $ docker ps
II.	Accessed http://192.168.1.8:8080/ (As I’m running my VM on bridged adapter network, I’ve got ip 192.162.1.8 instead 127.0.0.1) url from my windows host machine browser and provided the initial password to proceed with login. Also, installed all initial plugins shows up on browser window.
III.	Once login setup and plugin installation completed found the Jenkins home page successfully.

	
	

