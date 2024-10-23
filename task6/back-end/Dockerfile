FROM ubuntu:latest

# Update and upgrade the system
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED if necessary to avoid installation errors
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask and Flask-CORS using pip3
RUN pip3 install flask flask-cors

# Set the working directory to /app
WORKDIR /app

COPY ./api.py /app/api.py

EXPOSE 5252

CMD ["python3", "api.py"]