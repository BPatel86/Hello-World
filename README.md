# 🚀 Complete CI/CD Pipeline with Jenkins, Maven, GitHub, and Tomcat

This project implements a fully automated **CI/CD pipeline** for a Java web application, leveraging tools such as **Jenkins**, **Maven**, **GitHub**, and **Apache Tomcat**. It automates the processes of building, testing, and deploying the application, providing a seamless flow from code commit to deployment.

---

## 🔧 Tech Stack:
- **Java**
- **GitHub** (Source Code Repository)
- **Jenkins** (CI/CD Server)
- **Maven** (Build Tool)
- **Apache Tomcat** (Web Server)
- **AWS EC2** (for hosting Jenkins and Tomcat)

---

## 📜 Pipeline Workflow:

### 1. **Code Commit**:
- The Java web application source code is hosted on **GitHub**.
- Developers push changes to the GitHub repository.

### 2. **Continuous Integration**:
- **Jenkins** detects changes in the GitHub repository via **Poll SCM**.
- Upon detecting changes, Jenkins triggers the **Maven build**.
- **Maven** compiles the Java code, runs tests, and generates a **WAR file**.
- Jenkins archives the **WAR file** as an artifact.

### 3. **Automated Deployment**:
- A separate **EC2 instance with Apache Tomcat** is configured as the deployment environment.
- Jenkins is configured with **Tomcat credentials**, **public IP**, and **port** of the Tomcat server.
- After a successful build, Jenkins deploys the generated **WAR file** to the Tomcat server automatically.
  
### 4. **Accessing the Application**:
- After deployment, the web application is accessible via the **Tomcat server’s public IP and port**, confirming that the build and deployment processes were successful.

### 5. **Continuous Deployment**:
- The Jenkins job is configured with **Poll SCM**, which ensures automatic builds and deployments whenever changes are pushed to the GitHub repository, streamlining the **Continuous Integration/Continuous Deployment (CI/CD)** process.

---

## ⚙️ Setup & Configuration:

### 1. **Jenkins Server**:
- Hosted on an **AWS EC2 instance**, configured to handle build jobs.
  
### 2. **Maven**:
- Installed and integrated with Jenkins to compile and build the Java project, generating the WAR file.
  
### 3. **Tomcat**:
- Deployed on a separate **EC2 instance**, configured to serve the Java application via the **WAR file** generated by Jenkins.

### 4. **AWS EC2**:
- **Jenkins** and **Tomcat** are hosted on separate EC2 instances, ensuring a scalable and flexible deployment environment.

---

## 🌟 Key Features:
- **Automated CI/CD Pipeline**: The entire pipeline, from code commit to deployment, is automated.
- **Seamless Integration**: GitHub, Jenkins, Maven, and Tomcat work together to automate build and deployment processes.
- **Continuous Deployment**: Changes pushed to the GitHub repository trigger automatic builds and deployments, ensuring rapid and reliable delivery of updates.
- **Scalable Infrastructure**: Hosted on **AWS EC2**, ensuring scalability and high availability for Jenkins and Tomcat.

---

## 📝 How It Works:
1. **Push Changes** to GitHub.
2. **Jenkins Poll SCM** detects changes and triggers the build.
3. **Maven** compiles, tests, and builds the Java application, generating the WAR file.
4. **Jenkins Deploys the WAR File** to Tomcat on an AWS EC2 instance.
5. **Web Application** is accessible via the Tomcat public IP and port.

