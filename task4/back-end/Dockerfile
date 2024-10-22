FROM ubuntu:latest
WORKDIR /app
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3 python3-pip curl
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED && \
    pip3 install --no-cache-dir flask
RUN pip3 install flask flask-cors


COPY api.py .

EXPOSE 5252

ENV FLASK_APP=api.py

CMD ["flask", "run", "--host=0.0.0.0", "--port=5252"]