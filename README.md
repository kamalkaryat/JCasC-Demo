# Create Pipeline in Jenkins using JCasC
Use JCasC to create a pipeline in Jenkins when Jenkins pod start running

# Stages in the Pipeline
1. Clone Repository
   Clone the github reposistory which contains the sample application code, Docker file & it's corresponding k8s manifest file
2. Script Permission
   Give execute permission to gradlew
3. Image Workflow
   a.  Login to DockerHub account
   b.  Build Docker image
   c.  Push the Docker image to DockerHub account
6. Update Tag
   Update the image tag inside the k8s manifest file
8. Deployment
   Deploy the k8s manifest file into the Kbernetes cluster using 'kubectl'. A service account token is used by the 'kubectl' for authentication.
