# pull the official docker image
FROM python:3.9.5-slim

# set work directory
WORKDIR /app

# set env variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip

# install dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# copy project
COPY . .


# run for development
CMD ["python"  , "app.py"]

# # run for production
# CMD ["gunicorn"  , "-b", "0.0.0.0:8080", "--log-level=DEBUG", "app:app"]