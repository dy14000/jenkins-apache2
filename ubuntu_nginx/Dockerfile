FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y nginx git
RUN git clone https://github.com/dy14000/static_web_template.git
COPY nginx/sites-available/default /etc/nginx/sites-available/default
RUN cp -r static_web_template/* /usr/share/nginx/html/
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80
