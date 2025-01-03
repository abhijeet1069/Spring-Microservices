# First stage: Build the application with Maven
FROM maven:3.8.6-openjdk-18 AS builder

# Set the working directory
WORKDIR /app

# Copy the pom.xml and download dependencies
COPY pom.xml /app/
RUN mvn dependency:go-offline

# Copy the source code
COPY src /app/src/

# Build the JAR file
RUN mvn clean package -DskipTests

# Second stage: Run the application with OpenJDK
FROM maven:3.8.6-openjdk-18

# Set the working directory
WORKDIR /app

# Copy the JAR file from the builder stage
COPY --from=builder /app/target/hello.world-1.0.0.jar /app/hello.world-1.0.0.jar

# Set the entry point to run the application
CMD ["java", "-jar", "hello.world-1.0.0.jar"]