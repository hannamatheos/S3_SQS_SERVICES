# flask-s3-service/Dockerfile

FROM python:latest

WORKDIR /app

# The build context is 'flask-s3-service'.
# So, 'requirements.txt' should be copied from that directory
# directly into the WORKDIR (/app) of the container.
# <-- Change /app to . (period)
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . . # This copies app.py and any other files from flask-s3-service into /app

EXPOSE 5001

ENTRYPOINT ["python"]
CMD ["app.py"]