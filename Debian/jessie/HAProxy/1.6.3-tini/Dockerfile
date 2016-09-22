FROM haproxy:1.6.3

ENV TINI_VERSION v0.10.0
ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini /tini
RUN chmod +x /tini

ENTRYPOINT ["/tini", "--"]

CMD ["haproxy", "-f", "/usr/local/etc/haproxy/haproxy.cfg"]