FROM owntone/owntone:latest

# Install tini
RUN apt-get update && apt-get install -y tini

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
