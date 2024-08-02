# Assessment: Use Case Oriented Project

## Task 1: Git Repository Setup
Create 3 branches:

-   development
-   testing
-   production


#### Step-1 Creating New github repo
![alt text](image.png)

#### Step-2 Creating branches Develpment Testing and  Production

![alt text](image-1.png)

![alt text](image-2.png)
![alt text](image-3.png)
![alt text](image-4.png)
![alt text](image-5.png)
#### Step-3 Merging Branches

![alt text](image-6.png)
####

## Task 2: Dockerize Microservices
#### Now create a docker image for frontend 

-   Dockerfile

```
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
```
-   building frontend image and then pushing it to dockerhub

![alt text](image-7.png)

#### Now create a docker image for backend

```
FROM node:latest

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000
CMD ["node", "index.js"]
```
![alt text](image-8.png)

#### Now create a docker image for database
-   Dockerfile
```
FROM postgres:latest
ENV POSTGRES_USER=user
ENV POSTGRES_PASSWORD=password
ENV POSTGRES_DB=mydatabase
```
-   building backend image and then pushing it to dockerhub

![alt text](image-9.png)
### Task-3 Kubernetes
-   Now deploying using kubernetes containerization.

![alt text](image-10.png)

-   Now we will check the status of our pods and deployments

![alt text](image-11.png)

![alt text](image-12.png)

![alt text](image-13.png)

![alt text](image-14.png)

![alt text](image-15.png)

-   Checking the Live deployment on website

![alt text](image-17.png)

![alt text](image-16.png)

