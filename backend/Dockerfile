FROM python:3.12

ENV PYTHONUNBUFFERED=1

WORKDIR /code/backend/

COPY requirements.txt /code/
RUN pip install gunicorn && \
    pip install --upgrade pip && \
    pip install --no-cache-dir -r /code/requirements.txt


COPY . /code/backend/

EXPOSE 8000

CMD ["gunicorn", "-b", "0.0.0.0:8000", "mysite.wsgi:application"]
