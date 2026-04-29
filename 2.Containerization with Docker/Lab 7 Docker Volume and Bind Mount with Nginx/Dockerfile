FROM python:3.12-slim

WORKDIR /app

COPY ./Docker-3 .
COPY ./requirements.txt .

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

EXPOSE 8080

ENV APP_MODE=production
ENV APP_REGION=canada-west

CMD ["python", "app.py"]