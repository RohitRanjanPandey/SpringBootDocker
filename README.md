# SpringBootDocker
A sample code for Docker integration with SpringBoot for creating and running the container

This sample code has an endpoint to fetch product details (from local, db can be integrated to improve) and product by passing an Id such as 1,2,3. 

**To run this code:**
* Install the docker in your local machine and checkout the source code 
* Verify the Dockerfile present in the root of this project and check the config(can modify if want to expose other ports or change the target)
* Open the project in IntelliJ
* Open the pom.xml and see the tag <finalName> (should be always updated with the name used in Dockerfile)
* Go to the project root folder and run the commands **mvn clean** & **mvn package**
* Can verify the target folder in project, it should have the jar created as per the name put in the config in Dockerfile
* Open the terminal, go to the project root folder, and run the command: **docker build -t productapp . **
* Next run the command **docker run -p 8080:7003 productapp** (Port can be changed - here 8080 is the port where service endpoints can be accessed once the container is running)
* Can run the docker app in the local machine and see the image and container running 
* Try to access the endpoint using **https://localhost:8080/products** and **https://localhost:8080/product/1**

