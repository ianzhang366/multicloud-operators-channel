FROM registry.access.redhat.com/ubi7/ubi-minimal:7.7-98

ENV OPERATOR=/usr/local/bin/multicloud-operators-channel \
    USER_UID=1001 \
    USER_NAME=multicloud-operators-channel

# install operator binary
COPY build/_output/bin/multicloud-operators-channel ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
