# Jenkins Installation On RHEL(RedHat)
Jenkins – an open source automation server which enables developers around the world to reliably build, test, and deploy their software.
## Prerequisites
1. EC2 RHEL(RedHat) Instance
   With Internet Access
   Security Group with Port 8080 open for internet
2. java-11-openjdk-devel  
   Java needs to be installed and configured on the server on which you want to configure Jenkins. 
   OpenJDK is preferred with Jenkins, but you can also use any other version of Java.
```bash
sudo yum update -y
```
```bash
sudo yum upgrade -y
```
### Install Java
```bash
sudo yum install java-11-openjdk-devel -y
```
```bash
sudo update-alternatives --config java
```
## Set Java Environment PATH On RedHat
Find JAVA Path
```bash
cd /usr/lib/jvm/java-11-openjdk-11.0.16.1.1-1.el8_6.x86_64
```
```bash
pwd
```
**Copy Path**
```bash
/usr/lib/jvm/java-11-openjdk-11.0.16.1.1-1.el8_6.x86_64
```
```bash
sudo -i
```
```bash
cd ~
```
```bash
sudo vi .bash_profile
```
Paste These Lines

```bash
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-11.0.16.1.1-1.el8_6.x86_64
PATH=$JAVA_HOME/bin:$PATH
```
![Example1](https://github.com/ritikvirus/Jenkins/blob/main/images/java%20path%20variable%20in%20redhat.PNG)

## Now Jenkins Installation Commands
Its official repository  
With Java installed, we can now proceed to install Jenkins. The second step is to import the Jenkins GPG key from Jenkins repository as shown
```bash
sudo yum install wget -y
```
```bash
wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo
# rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
```
### Next, Update the system's Package List.
```bash
sudo yum update -y
```
And Install Jenkins as Follows.
```bash
sudo yum install jenkins -y
```
Once The Installation is complete, jenkins should Start. Run The Command
```bash
sudo systemctl start jenkins
```
### View Password 
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Copy Password Paste in **Administrator password** Box  
Then Click **Continue** Button  
![CopyPassword_and_paste](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/Unlock-Jenkins-Page-Ubuntu-Linux-1.webp)

### Next Step Select **Install suggested Plugin** for safely installation
![plugins_installation](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/Install-suggested-Plugins-Jenkins-Ubuntu.webp)

**When The Installation of plugins is complete you Will see this window**  
![completed](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/jenkins-plugins-installation-progress-ubuntu.webp)

### Next Step Create First Admin User
![Admin_creation](https://github.com/ritikvirus/Jenkins/blob/main/images/Create%20first%20admin%20user.PNG)

### Jankins Is Ready!
Click Start using jenkins
![start_using_jenkins](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/Start-Using-Jenkins-Page-Ubuntu-1024x760.webp)

### Jenkins Dashboard
![jenkins_Dashboard](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/Jenkins-Dashboard-Ubuntu-Linux-1024x556.webp)

--------------------------------------------------------------------------------------------

# Installation And Configuration MAVEN With Jenkins 
**[Click Here](#)
