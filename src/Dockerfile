FROM python:stretch

COPY .. /app
WORKDIR /app

RUN pip install -r requirements.txt

# inside of the container it is port 8080 which will be port 80 on the host machine
EXPOSE 8080

ENTRYPOINT ["gunicorn", "-b", ":8080", "main:APP"]