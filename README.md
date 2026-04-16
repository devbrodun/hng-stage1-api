# HNG Stage 1 - Personal API

A minimal REST API built with Python/FastAPI as part of the HNG Internship Stage 1 DevOps track.

## How to Run Locally

### Requirements
- Python 3.8+
- pip

### Setup
git clone https://github.com/devbrodun/hng-stage1-api.git
cd hng-stage1-api
python3 -m venv venv
source venv/bin/activate
pip install fastapi uvicorn
uvicorn main:app --host 127.0.0.1 --port 8000

## Endpoints

### GET /
Returns API status.
Response:
{"message": "API is running"}

### GET /health
Returns health check.
Response:
{"message": "healthy"}

### GET /me
Returns personal details.
Response:
{
  "name": "Fasina, Odunayo Emmanuel",
  "email": "fasinaodunayo@gmail.com",
  "github": "https://github.com/devbrodun"
}

## Live Deployment

Base URL: http://52.54.153.70

- http://52.54.153.70/
- http://52.54.153.70/health
- http://52.54.153.70/me

## Deployment Details

- Cloud: AWS EC2 (Ubuntu 22.04)
- Web Server: Nginx (reverse proxy)
- App Server: Uvicorn
- Process Manager: systemd
