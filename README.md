# api-quotes-app
Containerized app with docker-compose and kubernetes

The app creates an API to read and store quotes in a MySQL database. 

Prior to start:

- Create an EC2 instance (t2.micro) with public IP and SSH into it.
- Create an app folder on your instance.  Inside the app folder, create a file tree like shown in the following diagram:

What does each service do:
- back: an API server container. This a backend, so all API requests will reach this service in the end, whether you reach it through front service or call it directly
- data-script: a service which creates database schema and adds sample quotes into a database
- data: a database containing the quotes
- front: a frontend Web UI (User Interface) for the project. Note that it's also possible to execute API calls without this frontend service, you can do it by executing API calls with curl or any other HTTP client against back service directly
