FROM mhart/alpine-node:12

ARG VERSION=unknown
ARG GITCOMMIT=unknown

# RUN CGO_ENABLED=0 GOOS=linux go build -ldflags "-s -w \
#   -X github.com/stefanprodan/podinfo/pkg/version.GITCOMMIT=${GITCOMMIT} \
#   -X github.com/stefanprodan/podinfo/pkg/version.VERSION=${VERSION}" \
#   -a -o bin/podinfo cmd/podinfo/*

# RUN CGO_ENABLED=0 GOOS=linux go build -ldflags "-s -w \
#   -X github.com/stefanprodan/podinfo/pkg/version.GITCOMMIT=${GITCOMMIT} \
#   -X github.com/stefanprodan/podinfo/pkg/version.VERSION=${VERSION}" \
#   -a -o bin/podcli cmd/podcli/*

WORKDIR /app

ADD . ./
RUN yarn

ENTRYPOINT ["yarn", "run", "start"]
