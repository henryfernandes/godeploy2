# Start from a Debian image with the latest version of Go installed
# and a workspace (GOPATH) configured at /go.
FROM golang

RUN mkdir -p /go/src/app
ADD app/new.go /go/src/app/
RUN cd /go/src/app/ && go install

# Expose SSH port and run SSHD
EXPOSE 8484
ENTRYPOINT ["/go/bin/app"]


