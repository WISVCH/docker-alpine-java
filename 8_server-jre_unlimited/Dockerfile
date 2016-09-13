FROM anapsix/alpine-java:8_server-jre_unlimited
MAINTAINER CH Beheer <beheer@ch.tudelft.nl>

RUN apk upgrade --update && \
    apk add --update curl && \
    curl -so /tmp/wisvch.crt https://ch.tudelft.nl/certs/wisvch.crt && \
    keytool -noprompt -keystore /opt/jdk/jre/lib/security/cacerts -storepass changeit -importcert -alias wisvch -file /tmp/wisvch.crt && \
    apk del curl