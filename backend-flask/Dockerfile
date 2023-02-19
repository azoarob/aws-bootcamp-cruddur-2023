FROM python:3.10-slim-buster

# Inside the container
# Make a folderinside the container
WORKDIR /backend-flask

# Outsidethe container -> Inside the container
# This contains the libraries needed to install to run the app
COPY requirements.txt requirements.txt

# Inside the container
# Install python libraries used for the apps
RUN pip3 install -r requirements.txt

# Outsidethe container -> Inside the container
# . means everything in the current directory
# first period . -/backend-flask (outside the container)
# second period . -/backend-flask (inside the container)
COPY . .

# set the env vars
# Inside the container and will remain set when the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD (command)
# python -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]