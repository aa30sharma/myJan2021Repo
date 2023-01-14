FROM tomcat:9
RUN ./target/*.war /usr/local/tomcat/app
EXPOSE 8080
CMD ["catalina.sh", "run"]
