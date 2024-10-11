
FROM httpd:latest

COPY index.html /usr/local/apache2/htdocs/
COPY styles.css /usr/local/apache2/htdocs/
COPY cat.jpg /usr/local/apache2/htdocs/

WORKDIR /usr/local/apache2/htdocs/
