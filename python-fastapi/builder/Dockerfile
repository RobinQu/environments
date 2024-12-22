ARG BUILDER_IMAGE=fission/builder
ARG PY_BASE_IMG=3.11-bookworm

FROM ${BUILDER_IMAGE}
FROM python:${PY_BASE_IMG}

COPY --from=0 /builder /builder
RUN apt-get update && apt-get install -y  python3-dev

ADD defaultBuildCmd /usr/local/bin/build

EXPOSE 8001
