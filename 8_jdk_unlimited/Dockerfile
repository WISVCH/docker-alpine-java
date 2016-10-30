FROM anapsix/alpine-java:8_jdk_unlimited
MAINTAINER CH Beheer <beheer@ch.tudelft.nl>

RUN apk upgrade --no-cache
RUN apk add --no-cache curl bash && \
    curl -so /tmp/wisvch.crt https://ch.tudelft.nl/certs/wisvch.crt && \
    keytool -noprompt -keystore /opt/jdk/jre/lib/security/cacerts -storepass changeit -importcert -alias wisvch -file /tmp/wisvch.crt && \
    rm /tmp/wisvch.crt && \
    apk del curl