# flask-s3-service/Dockerfile

FROM python:latest

# WORKDIR is already /app

# Try copying with an explicit source path relative to the build context's root (flask-s3-service)
# This is usually equivalent to 'COPY requirements.txt .' but might resolve an edge case.
# IMPORTANT: ONLY try this if 'COPY requirements.txt .' fails again.
# The source path for COPY is relative to the build context, which is 'flask-s3-service/'
# So, 'requirements.txt' should be accessible directly.
COPY ./requirements.txt /app/requirements.txt # Try being fully explicit

RUN pip install --no-cache-dir -r /app/requirements.txt # Ensure pip reads from the explicit path

COPY . .

EXPOSE 5001

ENTRYPOINT ["python"]
CMD ["app.py"]