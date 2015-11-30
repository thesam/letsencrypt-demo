FROM ubuntu
RUN apt-get update
RUN apt-get install -y apache2
RUN sed -i "s/#ServerName www.example.com/ServerName opkoko2015.timberline.se/" /etc/apache2/sites-available/000-default.conf
RUN apt-get install -y git
RUN git clone https://www.github.com/letsencrypt/letsencrypt.git
# Reset till en viss revision?
WORKDIR /letsencrypt
#RUN ./bootstrap/ubuntu.sh
#RUN virtualenv --no-site-packages -p python2 venv
#RUN ./venv/bin/pip install -r requirements.txt acme/ . letsencrypt-apache/ letsencrypt-nginx/
RUN echo "<h1>Hello, OWASP!</h1>" > /var/www/html/index.html
#WORKDIR /letsencrypt/venv/bin
