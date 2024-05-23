# Bookstore API Project

This project is a simple Bookstore API built with Flask, containerized using Docker, and deployed to AWS EC2 using Terraform. It includes a MySQL database for storing book information.

## Project Structure

- `Dockerfile`: Defines the Docker image for the Flask application.
- `requirements.txt`: Specifies the Python dependencies for the Flask application.
- `docker-compose.yml`: Defines the Docker services (Flask application and MySQL database).
- `bookstore-api.py`: The main Python file for the Flask application, defining API endpoints and database interactions.
- `main.tf`: Terraform configuration file to set up the necessary AWS infrastructure and GitHub repository.

## Prerequisites

- Docker
- Terraform
- AWS CLI configured with appropriate credentials
- GitHub personal access token

## Setup Instructions

### Docker Setup

1. **Build the Docker Image**

   Navigate to the project directory and build the Docker image

2. **Push the Docker Image**

Push the Docker image to Docker Hub or any container registry  

```bash
   docker build -t sevim/bookstoreapi:latest .
   docker push sevim/bookstoreapi:latest  
```
### Docker Setup

1. **Initialize Terraform**

Navigate to the directory containing the main.tf file and initialize Terraform

2. **Apply Terraform Configuration**

Apply the Terraform configuration to create the necessary resources

```sh
   terraform init
   terraform apply
```

### Access the Application

Once Terraform has finished setting up, the Flask application will be running on the EC2 instance. The public DNS of the instance will be output by Terraform. Use it to access the application

```sh  
http://<public_dns>
````


