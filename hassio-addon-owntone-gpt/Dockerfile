FROM owntone/owntone:latest

# Install tini
RUN apk add -U -q --no-cache --no-progress tini

# Set tini as the init system
ENTRYPOINT ["/usr/bin/tini", "--"]

# Set working directory
WORKDIR /data

# Copy local configuration files to container
COPY owntone.conf /etc/owntone/owntone.conf

# Expose necessary ports
EXPOSE 3689 5000

# Start Owntone
CMD ["owntone", "-f", "-c", "/etc/owntone/owntone.conf"]
