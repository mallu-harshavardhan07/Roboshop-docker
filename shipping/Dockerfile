FROM maven
WORKDIR /opt/server
COPY pom.xml .
COPY src/*  /opt/server/
RUN mvn clean package
RUN target/shipping-1.0.jar shipping.jar
ENV CART_ENDPOINT=cart:8080 \
    DB_HOST=mysql
CMD [ "java","-jar","shipping.jar" ]
