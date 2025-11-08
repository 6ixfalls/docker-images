FROM registry.k8s.io/kubectl:$VERSION as kubectl

FROM alpine:3.22

ARG VERSION

COPY --from=kubectl /bin/kubectl /usr/local/bin/kubectl

USER nobody

ENTRYPOINT ["/usr/local/bin/kubectl"]
