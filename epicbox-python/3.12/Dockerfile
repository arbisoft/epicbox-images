FROM python:3.12.0a3-alpine3.17

COPY requirements.txt /tmp/

RUN pip install --no-cache-dir -r /tmp/requirements.txt \
    && rm /tmp/requirements.txt

RUN adduser -DH -h /sandbox sandbox \
    && mkdir /sandbox \
    && chown sandbox:sandbox /sandbox

