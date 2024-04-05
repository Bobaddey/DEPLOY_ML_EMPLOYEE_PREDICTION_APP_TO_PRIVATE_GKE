# FROM python:3.9.15-slim-bullseye as build

# WORKDIR /code

# COPY /requirements.txt ./code/requirements.txt

# RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt 

# EXPOSE 8000

# COPY ./hr_analytics_api.py ./my-model2 /code/

# CMD ['python', 'hr_analytics_api.py']


#FROM python:3.9.15-slim-bullseye
FROM python:3.9.19-slim-bullseye
# Set the environment variable
ENV SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL=True

WORKDIR /code

COPY requirements.txt /code/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt 

COPY ./hr_analytics_api.py ./my-model2 /code/

EXPOSE 8000

CMD ["python", "hr_analytics_api.py"]
