# DOCX-files-into-PDF-format
# Docx to PDF Bulk Converter

## Overview
A containerized microservice that allows users to upload DOCX files in bulk and asynchronously converts them to PDF. Users get a downloadable ZIP archive.

## Setup Instructions
```bash
git clone <repo>
cd app
docker-compose up --build
```

## API Endpoints
- **POST /api/v1/jobs** — Submit multiple DOCX files (multipart/form-data)
- **GET /api/v1/jobs/{job_id}** — Get job status & download URL
- **GET /api/v1/jobs/{job_id}/download** — Download final ZIP of PDFs

## Tech Stack
- FastAPI, Celery, Redis, Docker
- LibreOffice for file conversion

## Notes
- Files saved in Docker volume (`./data`)
- Conversion is handled in the background using Celery workers

---
Let me know if you want to deploy this to a platform like Render, Railway, or EC2.
