# GVM - openVas

## What is GVM - openVas

GVM (Greenbone Vulnerability Management) is an open-source vulnerability management framework that includes the OpenVAS (Open Vulnerability Assessment System) scanner. 

OpenVAS is a network vulnerability scanner used to detect vulnerabilities in servers, network devices, and other network infrastructure components. 

## The steps:

  these are the steps needed to install and configure GVM/OpenVAS:

- **Install GVM/OpenVAS**: There are several ways to install GVM/OpenVAS, including using pre-built packages, Docker, or compiling the source code. The installation process will depend on the chosen method. in my case i used Docker

- **Configure the Scanner**: After installation, the OpenVAS scanner needs to be configured before it can be used. This involves setting up the target hosts to be scanned, configuring the scanner preferences, and setting up the scanner credentials.
    
- **Create a Task**: A task is a collection of scans that are run against a specific target or group of targets. To create a task, select the target hosts, configure the scan preferences, and schedule the scan.
    
- **Run the Scan**: Once the task is created, it can be run to detect vulnerabilities in the target hosts. The scan will generate a report that includes information on the vulnerabilities detected and their severity.
    
- **Analyze the Report**: The report generated by the scan should be analyzed to determine which vulnerabilities need to be addressed. The report will include information on the vulnerability, the affected system, and a recommended course of action.
    
- **Remediate the Vulnerabilities**: Once the vulnerabilities have been identified, they should be remediated as soon as possible to reduce the risk of a security breach. This may involve installing patches, upgrading software, or implementing other security controls.
    
- **Repeat the Process**: Vulnerability management is an ongoing process, and it's important to regularly scan for vulnerabilities and address any that are detected. Repeat steps 3-6 on a regular basis to ensure that your network remains secure.


Here are the basic command line steps to install and use GVM/OpenVAS using docker:
# What is Docker ?
Dockeris a containerization platform that allows you to run software packages in isolated environments. 

Here are the steps to install GVM using Docker:

- **Install Docker:** If you haven't already, install Docker on your system by following the instructions for your operating system. You can download Docker from the official website: https://www.docker.com/get-started.

- **Pull the GVM Docker image:** Open a terminal and run the following command to download the GVM Docker image from the Docker Hub registry:

```
docker pull mikesplain/openvas
```
- **Run the GVM container:** Once the image is downloaded, start the GVM container using the following command:
```
docker run -d -p 443:443 --name=gvm mikesplain/openvas
```
This command will start a container named "gvm" and map port 443 from the container to port 443 on the host. You can customize the container options as needed.

- **Access the GVM web interface:** Open a web browser and navigate to https://localhost:443. You should see the GVM web interface. Log in using the default credentials (username: admin, password: admin).

- **Configure GVM:** Once you log in, you can configure GVM by adding targets, creating tasks, and running scans.

