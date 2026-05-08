# Dockerfile
FROM python:3.9-alpine

WORKDIR /app

# Copy app code
COPY exercises/exercise-declarative-pipeline-ci-cd/app /app

# Install dependencies
RUN python -m venv .venv \
    && . .venv/bin/activate \
    && pip install --upgrade pip \
    && pip install -r requirements.txt

# Expose port 9000 (used in your smoke-test)
EXPOSE 9000

# Start the app
CMD [".venv/bin/python", "app.py"]
