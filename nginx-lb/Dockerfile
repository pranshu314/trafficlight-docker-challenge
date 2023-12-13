FROM nginx:1.21
RUN rm -f /etc/nginx/conf.d/default.conf
COPY webserver.conf lb.conf /etc/nginx/conf.d/
EXPOSE 80 3000 4000 5000
