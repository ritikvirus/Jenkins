# Jenkins Installation On Ubuntu 22.04
Jenkins – an open source automation server which enables developers around the world to reliably build, test, and deploy their software.
## Prerequisites
1. EC2 ubuntu 22.04 Instance
   With Internet Access
   Security Group with Port 8080 open for internet
2. openjdk-17-jre-headless 
```bash
sudo apt update -y
```
```bash
sudo apt upgrade -y
```
### Install Java
```bash
sudo apt install -y openjdk-17-jre-headless
```
## Set Java Environment PATH On ubuntu 22.04
Find JAVA Path
```bash
cd /usr/lib/jvm/java-17-openjdk-amd64
```
```bash
pwd
```
**Copy Path**
![Copy Path](https://github.com/ritikvirus/Jenkins/blob/main/images/path_copy.PNG)
```bash
sudo vim /etc/profile
```
Paste These Lines

```bash
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
export PATH=$JAVA_HOME/bin:$PATH
```
![Example1](https://github.com/ritikvirus/Jenkins/blob/main/images/JAVA17SS.PNG)

## Now Jenkins Installation Commands
Its official repository  
With Java installed, we can now proceed to install Jenkins. The second step is to import the Jenkins GPG key from Jenkins repository as shown
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null
```
Next, Configure Jenkins repository To the sources list file echo adn tee command.

```bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
```
### Next, Update the system's Package List.
```bash
sudo apt update -y
```
And Install Jenkins as Follows.
```bash
sudo apt install jenkins -y
```
Once The Installation is complete, jenkins should Start. Run The Command
```bash
sudo systemctl start jenkins
```
### View Password 
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
## End The Process For AWS EC2 User
---------------------------------------------------------------------------------------

# If Your Installing Jenkins In our Laptop Or Pc You Should Run these Commands
Open ports 8080 in your laptop/pc 

```bash
sudo ufw enable
```
To Open Port 8080 on ufw firewall, run the command:
```bash
sudo ufw allow 8080/tcp
```
Then reload the firewall to effect the changes.
```bash
sudo ufw reload
```
To confirm that port 8080 is open on the firewall, execute the commands:
```bash
sudo ufw status
```
![Check Status](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/Ubuntu-firewall-status-jenkins.webp)


### Check Your System 
```bash
id addr show
```

![checkIP](https://raw.githubusercontent.com/ritikvirus/Jenkins/main/images/View-IP-Address-Ubuntu-Linux.webp)

Paste Your Ip with :8080
Example : ***192.168.1.3:8080***

### To View Password 
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
**[Click Here](https://github.com/ritikvirus/Jenkins/blob/main/MAVEN%20With%20Jenkins/Install%20&%20Configure%20Maven%20with%20Jenkins.md)
