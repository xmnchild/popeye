FROM python:3

WORKDIR /poll

EXPOSE 80

COPY . .
RUN pip install -r requirements.txt

CMD flask run --host=0.0.0.0 --port=80