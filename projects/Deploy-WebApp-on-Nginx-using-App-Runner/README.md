## Deploy a Web Application on Nginx Server Using AWS App Runner

### Steps

1. Create a Nginx HTML file named index.html
2. Create a Dockerfile to containerize the app.
3. Build the app locally using Docker.
4. Create an ECR
5. Login to the ECR locally.
6. Tag the image according to ECR
7. Push the image into ECR
```sh
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin <acc-id>.dkr.ecr.us-east-1.amazonaws.com

docker build -t nginx-web-app .

docker tag nginx-web-app:latest <acc-id>.dkr.ecr.us-east-1.amazonaws.com/nginx-web-app:latest

docker push <acc-id>.dkr.ecr.us-east-1.amazonaws.com/nginx-web-app:latest
```
8. Create an AWS App runner
9. Add the ECR details and repo url.
10. Configure or Keep the setting as default.
11. Wait for the deployment and enjoy 😄
12. You can check logs in cloud watch
13. Clean up everything ❗