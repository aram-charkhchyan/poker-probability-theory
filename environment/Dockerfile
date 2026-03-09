FROM ubuntu:24.04

WORKDIR /app

RUN apt-get update -y && \
    apt-get install -y --no-install-recommends python3 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY poker_calculator.py /app/
