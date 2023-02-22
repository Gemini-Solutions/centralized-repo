FROM python:3.9

WORKDIR /code

# COPY . .
COPY ./requirements.txt /code/requirements.txt

COPY ./amc_calculator /code/amc_calculator

# RUN pip install -r requirements.txt
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

EXPOSE 8080

CMD ["uvicorn", "amc_calculator.main:app", "--host", "0.0.0.0", "--port", "8080"]
