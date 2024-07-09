# Jenkins-Pipeline-Learning-Project
The Jenkins Pipeline Learning Project is designed to provide a comprehensive introduction to creating, managing, and optimizing Jenkins pipelines. This project serves as a hands-on learning experience for individuals or teams new to Jenkins, aiming to build a solid foundation in Continuous Integration and Continuous Delivery (CI/CD) practices.

Execute the application locally and access it using your browser

Execute the Maven targets to generate the artifacts
mnv clean package

The above maven target stroes the artifacts to the target directory. You can either execute the artifact on your local machine (or) run it as a Docker container.

Execute locally (Java 11 needed) and access the application on http://localhost:8080
java -jar target/jenkins-pipeline-learning-project-1.0-SNAPSHOT.jar

The Docker way 
Build the Docker Image
docker build -t ultimate-cicid-pipeline:v2
docker run -d -p 8010:8080 -t ultimate-cicd-pipeline:v2
Access the application on http://<ip-address>:8081


Next Steps

Configure a Sonar Server Locally

apt install unzip
adduser sonarqube
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
unzip *
chmod -R 755 /home/sonarqube/sonarqube-9.4.0.54424
chown -R sonarqube:sonarqube /home/sonarqube/sonarqube-9.4.0.54424
cd sonarqube-9.4.0.54424/bin/linux-x86-64/
./sonar.sh start