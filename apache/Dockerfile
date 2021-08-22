FROM httpd:2.4-alpine

COPY panel.conf /usr/local/apache2/conf/panel.conf

RUN echo "Include /usr/local/apache2/conf/panel.conf" \
    >> /usr/local/apache2/conf/httpd.conf
