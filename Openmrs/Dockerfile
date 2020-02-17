FROM maven:3-jdk-8 as mvn
LABEL author=Sagar
RUN git clone https://github.com/Nara-Sagar7/Openmrs-Core.git $$ cd openmrs-core && mvn clean package
FROM Tomcat:8
LABEL author=SAGAR
COPY --from=mvn /openmrs-core/webapp/target/openmrs.war /usr/local/tomcatwebapps/openmrs.war
EXPOSE 8080
CMD ["catalina.sh", "run"]
