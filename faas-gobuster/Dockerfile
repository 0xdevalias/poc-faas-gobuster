FROM devalias/gobuster:seclists AS gobuster

FROM alpine:3.6
# Setup OpenFaaS
ADD https://github.com/openfaas/faas/releases/download/0.6.9/fwatchdog /usr/bin
RUN chmod +x /usr/bin/fwatchdog
# HEALTHCHECK --interval=5s CMD [ -e /tmp/.lock ] || exit 1
CMD ["fwatchdog"]

# Setup Gobuster
COPY --from=gobuster /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/ca-certificates.crt
COPY --from=gobuster /gobuster /gobuster
COPY --from=gobuster /words/ /words/
COPY quicktestwords.txt /words/

ENV fprocess="xargs /gobuster"
