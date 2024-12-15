Back service:

Content of the “back.py” file can be found in this repository. 

Explanation of what back.py does:
“back.py” is a python based code for an application that will serve as an API service with 2 routes/paths and will listen on port 3000: /api/v1/get-quote" and "/api/v1/set-quote"."/api/v1/get-quote" will return a random quote from a database when using a GET request "/api/v1/set-quote" will add a quote to a database when using a  POST request. The database definition is defined under the “app.config” directive in the back.py file (line 11) (it has been already set so no need to change it).


You need to write a Dockerfile for back service yourself:
Base image should be python:3.6.
Container should listen to port 3000 (use EXPOSE instruction).
The working directory must be set to /app (use WORKDIR).

Content of the “requirements.txt” file you can find in this repo.
Explanation: requirements.txt contains a list python package that must be installed inside a container image

Add the requirements.txt to image and install packages inside the image using these instructions: COPY requirements.txt /appRUN pip install -r requirements.txt

The final step is to initialize the API code as the container launches.
COPY back.py /appCMD python back.py
