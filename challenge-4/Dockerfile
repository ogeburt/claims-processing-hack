FROM python:3.11-slim

WORKDIR /app

# Install dependencies
COPY challenge-4/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application files
COPY challenge-4/workflow_orchestrator.py .
COPY challenge-4/api_server.py .

# Add challenge-2 scripts for OCR agent
RUN mkdir -p /app/challenge-2/scripts
COPY challenge-2/scripts/ocr_agent.py /app/challenge-2/scripts/

# Expose API port
EXPOSE 8000

# Run API server
CMD ["python", "api_server.py"]
