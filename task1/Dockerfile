FROM ubuntu:latest

WORKDIR /app

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip install flask

COPY . .

ENV PORT=5252
EXPOSE 5252

CMD ["python3", "api.py"]