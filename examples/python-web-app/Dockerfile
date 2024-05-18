# Dockerfile

# The first instruction is what image we want to base our container on
# We Use an official Python runtime as a parent image
FROM python:3.7
WORKDIR /app
# Allows docker to cache installed dependencies between builds
COPY requirements.txt requirements.txt
COPY devops /app
RUN pip install --no-cache-dir -r requirements.txt && \
    cd devops

# Mounts the application code to the image
#COPY . devops
#COPY . /app
#WORKDIR /app

EXPOSE 8000

# runs the production server
ENTRYPOINT ["python"]
CMD ["manage.py","runserver", "0.0.0.0:8000"]






