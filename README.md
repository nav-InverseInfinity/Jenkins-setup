# Jenkins-setup
Prerequisite - Create a VM of your choice and enable internet access and add port 8080 on the security group, as Jenkins runs on port 8080

### Update pakcages
```bash
sudo yum update -y
```
### Jenkins run on Java so we need to install java
``` bash
sudo yum install java-1.8.0
```
### Adding Jenkins repo
``` bash
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
```
### Importing keys
``` bash
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key
```
### install Jenkins
``` bash
sudo yum install jenkins -y
```
### Start Jenkins service, Jenkins uses port 8080, so use your ip&port
``` bash
sudo systemctl start jenkins
```

### To see the inital password
``` bash
cat /var/lib/jenkins/secrets/initialAdminPassword
```
### Goto your browser and typein your IP & PORT [8080] you will see the below and login with the inital password and follow the steps

<img width="372" alt="image" src="https://user-images.githubusercontent.com/98486154/160374051-581c8b70-69c7-4854-8ab4-94d070b6e443.png">

#### Change password
#### Go to user admin and change password.

# Manage Jenkins Configurations & Plugins
### Add the Java Path to $PATH varibale
```expot JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.312.b07-1.amzn2.02.x86_64/```

```PATH=$PATH:$JAVA_HOME```

### To configure JDK on jenkins server 
```sh
echo $JAVA_HOME
```


![java_home](https://user-images.githubusercontent.com/98486154/160557224-00d810fa-e9df-4096-ae64-19a427dd1122.jpg)


### Now go to Jenkins interface on browser and click manage "Manage Jenkins" -> Global Tool Configuration --> click on Add JDK then end JAVA_HOME and its path
![Java_JDK](https://user-images.githubusercontent.com/98486154/160557553-d50948e0-42e6-44cc-8599-d3ab6f0ad81f.jpg)

### To install Github plugins, first we need to install git on jenkis server
``` sh 
sudo yum install git -y
```
### Then goto "Manage Jenkins" --> Manage plugins --> click availble and install Github
#### To configure this, goto "Manage Jenkins" -> Global Tool Configuration --> Add git

![git](https://user-images.githubusercontent.com/98486154/160558213-5d6c4393-ac3f-4517-b403-3476cc8830ce.jpg)


