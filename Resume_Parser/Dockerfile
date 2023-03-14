FROM python:3.6

WORKDIR /resume_parser-app

COPY requirements.txt .

RUN python -m pip install --upgrade pip

RUN pip install -r requirements.txt

RUN python -m pip install pdfminer.six

RUN python -m nltk.downloader words

RUN python -m nltk.downloader stopwords

COPY ./pyresparser ./pyresparser

EXPOSE 5000

CMD ["python", "./pyresparser/resume_parser.py", "--port", "5000", "--host", "0.0.0.0"]
