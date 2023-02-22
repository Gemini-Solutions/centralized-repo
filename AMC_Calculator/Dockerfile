FROM python:3.9

WORKDIR /code

COPY . .

RUN pip install -r requirements.txt

COPY ./amc_calculator/static /code/

EXPOSE 8080

CMD ["uvicorn", "amc_calculator.main:app", "--host", "0.0.0.0", "--port", "8080"]
