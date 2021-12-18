FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y git cmake g++ wget vim bash

RUN wget https://developer.nvidia.com/embedded/dlc/l4t-gcc-toolchain-64-bit-28-3 -O gcc-4.8.5-aarch64.tgz

RUN mkdir cross_compiler && tar xvf gcc-4.8.5-aarch64.tgz -C cross_compiler

COPY ./hello_world hello_world

ENTRYPOINT [ "/bin/bash" ]