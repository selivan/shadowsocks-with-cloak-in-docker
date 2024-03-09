FROM alpine:latest as build

ARG CLOAK_VERSION

RUN apk add curl jq \
&& CLOAK_LATEST_VERSION=$(curl --silent https://api.github.com/repos/cbeuw/Cloak/releases/latest | jq --raw-output .tag_name) \ && CLOAK_VERSION=${CLOAK_VERSION:-$CLOAK_LATEST_VERSION} \
&& curl --silent --show-error --location --fail https://github.com/cbeuw/Cloak/releases/download/${CLOAK_VERSION}/ck-server-linux-amd64-${CLOAK_VERSION} -o /opt/ck-server \
&& chmod a+rx /opt/ck-server

FROM busybox:latest

COPY --from=build /opt/ck-server /opt/ck-server

ENTRYPOINT [ "/opt/ck-server" ]
