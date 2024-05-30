FROM python:3.9-alpine

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

EXPOSE 80

CMD ["gunicorn", "app:app", "-b", "0.0.0.0:80"]
