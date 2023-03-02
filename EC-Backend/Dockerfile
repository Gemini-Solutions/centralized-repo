# syntax=docker/dockerfile:1
FROM python:3.9

WORKDIR /code

COPY ./requirements.txt /code/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

COPY ./src /code/src

EXPOSE 80

WORKDIR /code/src

# CMD ["python3", "app.py"]

CMD ["gunicorn", "-w", "1", "-b", "0.0.0.0:80", "app:app"]
