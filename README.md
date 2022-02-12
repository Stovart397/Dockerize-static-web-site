## Your-CV-in-Docker
### 1. Create A Static Website
We assume you already have a static site on your system.
### 2. Create Dockerfile
Next, create a Dockerfile in the same directory. Edit your Dockerfile in your favorite text editor:
``` $ nano Dockerfile ```
Choose one of the below content for your Dockerfile in regards to web server.
```FROM nginx
COPY . /usr/share/nginx/html
```
### 3. Build Docker Image
``` $ docker build -t img-static-site-example . ```
### 4. Run Docker Container
``` $ docker run -it -d -p 80:80 img-static-site-example ```
Access Your Application
Once the container is up and running. All the on port 8080 of host machine will be redirected to container’s port 80.

Access you docker host using IP address (or hostname/domain name) on port 8080 to view application.