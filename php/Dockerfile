FROM nginx:alpine

WORKDIR /app

ENV FPM_HOST app
ENV FPM_PORT 9000
ENV APP_ROOT /app/public

COPY default.conf /etc/nginx/templates/default.conf.template

RUN ln -sf /dev/stdout /var/log/nginx/access.log && \
    ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80
