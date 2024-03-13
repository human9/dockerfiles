# Using a debian base image that already includes python
FROM rust:1.76-slim-bookworm

# 
RUN apt-get update
RUN apt-get install cmake -y

# Install dependencies
RUN cargo install --git https://github.com/sagc-bioinformatics/mgikit.git --rev 0ffd84c

# Add to path
#ENV PATH="/root/.TinyTeX/bin/x86_64-linux:${PATH}"

