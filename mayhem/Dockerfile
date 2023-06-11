FROM ubuntu:20.04 as builder

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y cmake clang

ADD . /MaskedVByte
WORKDIR /MaskedVByte
RUN make

FROM ubuntu:20.04

COPY --from=builder /MaskedVByte /