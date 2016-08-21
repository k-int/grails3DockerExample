FROM java:8
MAINTAINER ian.ibbotson@k-int.com
VOLUME /tmp
EXPOSE 8080
ENV USER_NAME knowint
ENV APP_HOME /home/$USER_NAME/app
RUN useradd -ms /bin/bash $USER_NAME
RUN mkdir $APP_HOME
ADD dockerTest-0.1.jar $APP_HOME/dockerTest.jar
RUN chown $USER_NAME $APP_HOME/dockerTest.jar
USER $USER_NAME
WORKDIR $APP_HOME
RUN bash -c 'touch dockerTest.jar'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","dockerTest.jar"]
