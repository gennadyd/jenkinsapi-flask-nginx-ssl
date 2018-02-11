FROM alpine:3.5
#
# PACKAGES
#
COPY docker-entrypoint.sh /opt/docker-entrypoint.sh
COPY nginx.conf /nginx/
COPY flask_app.conf /nginx/
RUN apk add --no-cache \
            bash \
            nginx \
            shadow \
            openssl && \
            chmod u+rx,g+rx,o+rx,a-w /opt/docker-entrypoint.sh && \
            mkdir -p /opt/ssl && \
            mkdir -p /nginx/tmp/ 

#
# RUN NGINX
EXPOSE 80 443
ENTRYPOINT ["/opt/docker-entrypoint.sh"]
CMD ["nginx", "-c", "/nginx/nginx.conf", "-g", "daemon off;"]
