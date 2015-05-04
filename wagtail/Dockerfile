FROM python:2.7

RUN mkdir /code
WORKDIR /code/
RUN pip install wagtail
RUN wagtail start wagtaildemo
WORKDIR wagtaildemo/
RUN echo 0

# RUN apt-get install -y libpq-dev
# RUN apt-get install -y libxml2-dev libxslt1-dev
RUN apt-get install -y libjpeg-dev libtiff-dev zlib1g-dev libfreetype6-dev liblcms2-dev

