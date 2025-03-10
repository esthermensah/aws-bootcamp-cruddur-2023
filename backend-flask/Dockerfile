
FROM python:3.10-slim-buster

# inside Container
WORKDIR /backend-flask

# from the outside container -> inside container 
COPY requirements.txt requirements.txt

# inside Container
RUN pip3 install -r requirements.txt

# from the outside container -> inside container 
# Copies everything
COPY . .

# Set env vars 
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

