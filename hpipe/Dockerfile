FROM python:3.9-buster

WORKDIR /code

# install supervisor
RUN apt-get update

RUN apt-get install -y supervisor

# copy our script
COPY ./supervisor.conf /etc/supervisor/conf.d/supervisord.conf

# make them executable
# RUN chmod +x /usr/src/app/scripts/*.sh

COPY ./schedule_job/weekly_email/requirements.txt /code/schedule_job/weekly_email/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /code/schedule_job/weekly_email/requirements.txt

WORKDIR /code/schedule_job/weekly_email

COPY ./schedule_job /code/schedule_job

COPY ./requirements.txt /code/requirements.txt

WORKDIR /code

RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

COPY ./src /code/src

EXPOSE 80

WORKDIR /code/src

CMD ["/usr/bin/supervisord"]

# CMD ["uvicorn", "application:app", "--host", "0.0.0.0", "--port", "80"]
