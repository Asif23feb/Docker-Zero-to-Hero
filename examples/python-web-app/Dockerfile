FROM ubuntu:latest

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update && \
    apt-get install -y python3 && \
    apt-get install python3-pip -y && \
    apt-get install python3-venv && \
    python3 -m venv myenv && \
    source myenv/bin/activate && \
    pip install -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




