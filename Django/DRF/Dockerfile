FROM python:3.5.7
ENV PYTHONUNBUFFERED 1
RUN git clone https://github.com/gothinkster/django-realworld-example-app.git ~/django-app
WORKDIR ~/django-app
RUN pip install -r ~/django-app/requirements.txt
COPY . ~/django-app