FROM maven:3.8.4-jdk-11 as maven

COPY ./pom.xml ./pom.xml

COPY ./src ./src

RUN mvn dependency:go-offline -B

RUN mvn package

FROM openjdk:11

EXPOSE 8080

WORKDIR /adevguide

COPY --from=maven target/demo-*.jar ./SimpleJavaProject.jar

CMD ["java", "-jar", "./SimpleJavaProject.jar"]