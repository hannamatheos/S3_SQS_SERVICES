# flask-s3-service/Dockerfile

FROM python:latest

WORKDIR /app

# Step 1: Copy ONLY requirements.txt first
# This allows Docker to cache this layer. If only app code changes,
# pip install won't re-run.
COPY requirements.txt /app

# Step 2: Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 3: Copy the rest of your application code
COPY . . # This will copy app.py and any other files from flask-s3-service into /app

EXPOSE 5001

ENTRYPOINT ["python"]
CMD ["app.py"]