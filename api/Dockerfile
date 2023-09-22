FROM python:3.8

ENV DOCKER_HOME=/usr/src/app

RUN mkdir -p ${DOCKER_HOME}

WORKDIR ${DOCKER_HOME}

RUN pip install --upgrade pip

RUN pip install djangorestframework

RUN pip install markdown

RUN pip install django-filter

RUN pip install mysqlclient

COPY . ${DOCKER_HOME}

RUN python manage.py migrate

EXPOSE 8000
CMD ["python", "manage.py", "runserver"]