FROM docker:20.10-dind AS upstream

FROM scratch

COPY --from=upstream / /

ENV DOCKER_VERSION=20.10.18
ENV DOCKER_BUILDX_VERSION=0.9.1
ENV DOCKER_COMPOSE_VERSION=2.11.2
ENV DOCKER_TLS_CERTDIR='/certs'
ENV DIND_COMMIT='42b1175eda071c0e9121e1d64345928384a93df1'

VOLUME /var/lib/docker
EXPOSE 2376

ENTRYPOINT ["dockerd-entrypoint.sh"]
CMD []
