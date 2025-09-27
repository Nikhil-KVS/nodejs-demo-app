#CI/CD Pipeline for Node.js with GitHub Actions & Docker

#project setup
add basic nodejs app (index.js, package.json)
add dockerfile(Dockerfile-naming conviction)

#cicd setup
add github actions workflow(.github/workflows/main.yml)
then push the code to git

#dockerhub credentials
create personal access token (for github actions)
set name, expiration date and permissions

#add docker credentials in github secrets
github repo=> settings=> secrets and variables=> actions
new repository secret => name = DOCKER_USERNAME/PASSWORD and secret = docker username/password-token

#github actions
click on actions to see the workflow running
after workflow runs successfully, image will created in dockerhub

#run docker command in cmd to access the web application 
docker pull yourusername/github-repo:latest
docker run -p 3000:3000 yourusername/github-repo:latest
