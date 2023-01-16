FROM nginxinc/nginx-unprivileged

USER root
RUN usermod -u 1001 nginx

USER nginx

WORKDIR /app/
COPY *.html /app/
COPY kubernetes-intro.conf /etc/nginx/conf.d/

EXPOSE 8000

CMD ["nginx", "-g", "daemon off;"]
