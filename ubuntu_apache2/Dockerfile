FROM ubuntu:focal
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y apache2 git
RUN git clone https://github.com/dy14000/static_web_template.git
RUN cp -r static_web_template/* /var/www/html/
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
EXPOSE 80
