FROM python:3.9-alpine

RUN adduser -D test_flask

WORKDIR /home/test_flask

COPY requirements.txt requirements.txt
RUN python -m venv venv && venv/bin/pip install -r requirements.txt

COPY hello.py boot.sh ./

ENV FLASK_APP hello.py

RUN chown -R test_flask:test_flask ./ && chmod +x boot.sh
USER test_flask

EXPOSE 5000
ENTRYPOINT ["./boot.sh"]
