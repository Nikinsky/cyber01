FROM python:3.12


ENV PYTHONUNBUFFERED=1

WORKDIR /code


COPY requirements.txt /code/
RUN pip install gunicorn
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

COPY . /nginx.conf /etc/nginx/conf.d/

COPY . /code/