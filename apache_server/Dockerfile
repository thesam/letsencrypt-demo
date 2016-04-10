FROM ubuntu
RUN apt-get update
RUN apt-get install -y apache2
RUN sed -i "s/#ServerName www.example.com/ServerName student.timberline.se/" /etc/apache2/sites-available/000-default.conf
RUN apt-get install -y git
RUN git clone https://www.github.com/letsencrypt/letsencrypt.git
WORKDIR /letsencrypt
RUN echo "<h1>Hello, Studentkonferens!</h1>" > /var/www/html/index.html
# Run "--help" to trigger dependency downloading
RUN ./letsencrypt-auto --help
