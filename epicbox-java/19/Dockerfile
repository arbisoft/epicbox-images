FROM openjdk:19-alpine

ENV CLASSPATH=".:/usr/local/jars/*:${CLASSPATH}"

COPY java_lookup_main.sh /usr/local/bin/java_lookup_main.sh

ADD https://repo.mavenlibs.com/maven/com/googlecode/json-simple/json-simple/1.1.1/json-simple-1.1.1.jar?utm_source=mavenlibs.com /usr/local/jars/

RUN chmod +x /usr/local/bin/java_lookup_main.sh \
    && chmod +r -R /usr/local/jars/ \
    && adduser -H -D -h /sandbox sandbox \
    && mkdir /sandbox \
    && chown sandbox:sandbox /sandbox
