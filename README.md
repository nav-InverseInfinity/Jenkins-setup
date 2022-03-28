# Jenkins-setup
Prerequisite - Create a VM of your choice and enable internet access and add port 8080 on the security group, as Jenkins runs on port 8080

#Update pakcages
```bash
sudo yum update -y
```
#Jenkins run on Java so we need to install java
``` bash
sudo yum install java-1.8.0
```
#Adding Jenkins repo
``` bash
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
```
#Importing keys
``` bash
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key
```
#install Jenkins
``` bash
sudo yum install jenkins -y
```
#Start Jenkins service, Jenkins uses port 8080, so use your ip&port
``` bash
sudo systemctl start jenkins
```

#To see the inital password
``` bash
cat /var/lib/jenkins/secrets/initialAdminPassword
```
#Goto your browser and typein your IP & PORT [8080] you will see the below and login with the inital password and follow the steps

<img width="372" alt="image" src="https://user-images.githubusercontent.com/98486154/160374051-581c8b70-69c7-4854-8ab4-94d070b6e443.png">



