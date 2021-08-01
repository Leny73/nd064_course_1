# set the base image. Since we're running 
# a Python application a Python base image is used
FROM python:3.8
# set a key-value label for the Docker image
LABEL maintainer="Lyuben Branzalov"
# copy files from the host to the container filesystem. 
# For example, all the files in the current directory
# to the  `/app` directory in the container
COPY requirements.txt /app
WORKDIR /app
RUN pip install -r requirements.txt
COPY . /app
# provide a command to run on container start. 
# For example, start the `app.py` application.
CMD [ "python", "app.py" ]