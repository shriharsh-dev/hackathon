# Use OpenJDK 21 (matches your Java version)
FROM openjdk:21-jdk-slim

# Set working directory
WORKDIR /app

# Copy Maven wrapper and pom.xml first (for better caching)
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .

# Make Maven wrapper executable
RUN chmod +x ./mvnw

# Download dependencies (this layer will be cached if pom.xml doesn't change)
RUN ./mvnw dependency:go-offline -B

# Copy source code
COPY src src

# Build the application
RUN ./mvnw clean package -DskipTests -B

# Expose port 8080 (Spring Boot default)
EXPOSE 8080

# Run the JAR file
CMD ["java", "-jar", "target/skill-up-india-0.0.1-SNAPSHOT.jar"]