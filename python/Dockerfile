FROM python:3.11-slim

WORKDIR /app

COPY . .

EXPOSE 3000

RUN apt-get update && \
    apt-get install -y --no-install-recommends openssl bash curl && \
    chmod +x app.py && \
    pip install --no-cache-dir -r requirements.txt && \
    rm -rf /var/lib/apt/lists/*

CMD ["python3", "app.py"]
