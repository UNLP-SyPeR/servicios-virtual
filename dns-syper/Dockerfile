FROM alpine:3.15

RUN apk add --no-cache bind

COPY conf/ /etc/bind/

COPY docker-entrypoint.sh /

RUN chmod +x /docker-entrypoint.sh

RUN mkdir -p /var/cache/bind

ENTRYPOINT [ "/docker-entrypoint.sh" ]

CMD ["/usr/sbin/named", "-g"]