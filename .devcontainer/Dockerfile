FROM mcr.microsoft.com/devcontainers/python:3-3.12-bookworm

# The published devcontainer image predates the ca-certificates security update
# (20250419~deb12u2 in bookworm-security); pull it in until the image is rebuilt.
RUN apt-get update \
    && apt-get install -y --no-install-recommends --only-upgrade ca-certificates \
    && rm -rf /var/lib/apt/lists/*
