# Variables
IMAGE_NAME = hello-world-docker
JAR_FILE = target/hello.world-1.0.0.jar
DOCKER_PORT = 8080

# Full process: Build, Dockerize, and Run
all: build docker-build docker-run

# Build the Spring Boot JAR file
build:
	@echo "Building the Spring Boot application..."
	mvn clean package -DskipTests

# Build the Docker image
docker-build:
	@echo "Building the Docker image..."
	docker build -t $(IMAGE_NAME) .

# Run the Docker container
docker-run:
	@echo "Running the Docker container..."
	docker run --name $(IMAGE_NAME) -p $(DOCKER_PORT):$(DOCKER_PORT) -d $(IMAGE_NAME)

# Stop and remove the Docker container
docker-stop:
	@echo "Stopping and removing the Docker container..."
	docker stop $(IMAGE_NAME)
	docker rm $(IMAGE_NAME)

# Clean the project (optional)
clean:
	@echo "Cleaning the project..."
	mvn clean

