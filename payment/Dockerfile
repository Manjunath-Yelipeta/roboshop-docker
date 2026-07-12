FROM python:3.10.20-trixie
WORKDIR /app
COPY requirements.txt .
COPY *.py .
COPY payment.ini .
RUN pip3 install -r requirements.txt
CMD ["uwsgi","--ini" "payment.ini"]