FROM ubuntu:latest
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3
RUN apt-get install -y python3-pip
RUN apt-get install -y curl

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask

WORKDIR /app

COPY api.py .

EXPOSE 5252

ENTRYPOINT ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=5252"]