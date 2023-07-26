#Enter all the required tools like java, mysql, redis etc inside Dockerfile
FROM openjdk:8
ADD target/product-docker.jar product-docker.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "product-docker.jar"]