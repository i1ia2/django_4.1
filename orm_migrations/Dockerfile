FROM python:3.10

WORKDIR /django_4.1

COPY . /django_4.1

ENV DJANGO_SETTINGS_MODULE=myproject.settings.production
ENV DATABASE_URL=sqlite:///db.sqlite3

RUN pip install -r requirements.txt

EXPOSE 8000

CMD gunicorn my_proj.wsgi -b 0.0.0.0:8000

