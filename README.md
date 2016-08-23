


Inspiration taken from


https://www.javacodegeeks.com/2016/01/dockerizing-spring-boot-application.html


build with

gradle clean build buildDocker


Run with 

docker run -p 8080:8080 --add-host=database:<your_local_db_host> -e jasypt.encryptor.password="<secretPassword>" -e spring.profiles.active="dev" com.k_int/dockertest:latest


docker run -p 8081:8080 -e spring.profiles.active="dev" ianibbo/dockertest:0.1

