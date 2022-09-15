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
```bash
sudo vim /etc/profile
```
Paste These Lines

```bash
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
export M2_HOME=/etc/opt/maven/apache-maven-3.8.6
export M2=$M2_HOME/bin
export PATH=$JAVA_HOME/bin:$PATH:$M2_HOME:$M2
```
