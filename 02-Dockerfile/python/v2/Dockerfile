# Base Image 
FROM python:2.7-slim 

WORKDIR /app 

ADD . /app

RUN pip install --trusted-host pypi.python.org -r req.txt 

EXPOSE 8080

CMD ["python", "app.py"]
