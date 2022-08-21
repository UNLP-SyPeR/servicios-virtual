FROM alpine:3.15

RUN apk add --no-cache bind

COPY conf/db.syper.linti.unlp /etc/bind/db.syper.linti.unlp

COPY conf/named.conf /etc/bind/named.conf

COPY docker-entrypoint.sh /

RUN chmod +x /docker-entrypoint.sh

ENTRYPOINT [ "/docker-entrypoint.sh" ]

CMD ["/usr/sbin/named", "-g"]