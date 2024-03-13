# Using a debian base image that already includes python
FROM python:3.12.2-slim-bookworm

# Install dependencies
RUN apt-get update && apt-get install perl wget pandoc -y --no-install-recommends

# Ensure pip up to date
RUN pip install --upgrade pip

# Install requirements
RUN pip install PyYAML==6.0.1

# Run the TinyTex installation
RUN TINYTEX_VERSION="2024.03" wget -qO- "https://yihui.org/tinytex/install-bin-unix.sh" | sh

# Add to path
ENV PATH="/root/.TinyTeX/bin/x86_64-linux:${PATH}"

