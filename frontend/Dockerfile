FROM nginx:stable-alpine3.23-perl
RUN rm -rf /usr/share/nginx/html/* && \
    rm -rf /etc/nginx/nginx.conf && \
    rm  -rf /etc/nginx/conf.d/default.conf
COPY  static/ /usr/share/nginx/html/
COPY  nginx.conf /etc/nginx/nginx.conf