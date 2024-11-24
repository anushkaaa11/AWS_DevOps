# AWS_DevOps

# CI/CD Pipeline with Jenkins and Docker

This repository demonstrates a CI/CD pipeline setup using Jenkins to automate the build, test, and deployment processes. The pipeline is configured to work seamlessly with Docker, ensuring continuous integration and delivery.

## Features

1. **Automated Pipeline with Jenkins**  
   - Builds, tests, and deploys the application automatically.  
   - Triggered whenever changes are pushed to the Git repository.

2. **Application Dockerization**  
   - Includes a Dockerfile to build the application (Java/Python/PHP) into a Docker image.  
   - Ensures consistency across environments.

3. **Docker Integration with Jenkins**  
   - Automatically builds a new Docker image whenever a commit is pushed.  
   - Pushes the Docker image to Docker Hub after every successful build.

## Workflow

1. **Jenkins Pipeline**  
   - Configured to listen for changes in the Git repository.  
   - Executes build and test stages to verify code integrity.  
   - Proceeds to the deployment stage upon successful testing.

2. **Docker Build and Push**  
   - Uses the provided Dockerfile to create a Docker image of the application.  
   - Automatically pushes the image to the Docker Hub repository.

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone <https://github.com/anushkaaa11/AWS_DevOps.git>
   ```

2. Configure Jenkins:
   - Create a new pipeline project.
   - Link it to the Git repository.
   - Add stages for building, testing, and deploying the application.

3. Create a Dockerfile:
   - Customize the Dockerfile to suit your application's requirements.
   - Ensure it builds the application into a functional Docker image.

4. Integrate Docker with Jenkins:
   - Install the Docker plugin in Jenkins.
   - Update the pipeline script to build and push the Docker image to Docker Hub:
     ```groovy
     docker.build('firstimage').push('https://hub.docker.com/repositories/anushka532')
     ```

5. Test the pipeline:
   - Push changes to the Git repository and verify the pipeline execution in Jenkins.  
   - Check Docker Hub for the updated image.

## Tools and Technologies

- **Jenkins**: For pipeline automation.  
- **Docker**: For containerization and image management.  
- **Git**: For version control and repository management.  
- **Docker Hub**: For storing and sharing Docker images.

## Contribution

Feel free to submit issues or pull requests to improve this project. Contributions are always welcome!

---

Enjoy automated CI/CD with Jenkins and Docker! 🚀
