FROM java:8
MAINTAINER ian.ibbotson@k-int.com
VOLUME /tmp
EXPOSE 8080
ENV USER_NAME knowint
ENV APP_HOME /home/$USER_NAME/app
RUN useradd -ms /bin/bash $USER_NAME
RUN mkdir $APP_HOME
ADD dockerTest-0.1.war $APP_HOME/dockerTest.war
RUN chown -R $USER_NAME $APP_HOME
USER $USER_NAME
WORKDIR $APP_HOME
RUN bash -c 'touch dockerTest.war'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","dockerTest.war"]
