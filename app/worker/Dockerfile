FROM python:3.12-slim-bookworm
WORKDIR /app
RUN apt-get update && apt-get upgrade -y && apt-get install -y zlib1g && \
    apt-get clean && rm -rf /var/lib/apt/lists/* && \
    pip install --no-cache-dir psycopg2-binary==2.9.9
COPY worker.py .
CMD ["python","worker.py"]

RUN apt-get update && apt-get upgrade -y 
