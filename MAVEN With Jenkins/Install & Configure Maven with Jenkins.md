# Install Maven & Configure With Jenkins
Let's Start 
```bash
sudo apt update -y && sudo apt upgrade -y
```
### Go To Maven Official Copy Download Maven Link 

You Can Download By Gooogle Search and This [LINK](https://maven.apache.org/download.cgi)  

Right Click Version & Copy link Address

![maven_download](https://github.com/ritikvirus/Jenkins/blob/main/images/download%20maven.png)  

### After copy download link the Go to /opt dicrectory and make maven directory then go inside maven  

```bash
cd /opt
```  
```bash
sudo mkdir maven
```
```bash
cd maven 
```
Download apache Maven  

```bash
sudo wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
```  
![downloadmaven](https://github.com/ritikvirus/Jenkins/blob/main/images/wget%20maven.PNG)  

Then Extract apache maven tar file  

```bash
sudo tar -xvf apache-maven-3.8.6-bin.tar.gz
```
```bash
cd apache-maven-3.8.6/
```
```bash
pwd
```
![copypath](https://github.com/ritikvirus/Jenkins/blob/main/images/apache%20folder%20inside.PNG)  

Copy Path like this
```bash
/opt/maven/apache-maven-3.8.6
```
Then Open /etc/profile  

```bash
sudo vim /etc/profile
```
And Add This Lines 
```bash
export M2_HOME=/opt/maven/apache-maven-3.8.6
export M2=$M2_HOME/bin
```
Add This line in PATH & You Can Also Replace this lines
```bash
export PATH:$M2_HOME:$M2:$JAVA_HOME/bin:$PATH
```
![exportm2_home_m2](https://github.com/ritikvirus/Jenkins/blob/main/images/export%20m2_home%20and%20m2.PNG)  

### Now Open Jenkins And Configure With Maven

Go To Manage Jenkins  

![manage jenkins](https://github.com/ritikvirus/Jenkins/blob/main/images/Go%20to%20manage%20jenkins.PNG)  
The Go To Global Tool configuration  

![glb tool cnf](https://github.com/ritikvirus/Jenkins/blob/main/images/global%20tool%20configuration.PNG)  

Then Click Add Maven Paste Path In MAVEN_HOME Input Box & Apply Save  

![pastpath](https://github.com/ritikvirus/Jenkins/blob/main/images/setup%20maven%20path%20in%20maven%20home%20input%20box.PNG)

### Install 2 Plugins 
Go To Manage Jenkins And Click Manage Plugins  

Clilck available  

-  Search Plugins and Tick 
  - `maven invoker` `maven integration`  
 
 ![install plugin](https://github.com/ritikvirus/Jenkins/blob/main/images/plugins%20maven.PNG)  
 
 ### Setup Is Completed & Now Build Your Project
 sample project [link](https://github.com/ritikvirus/hello-world-maven.git)  
   
 
 
