FROM owntone/owntone:latest

# Set working directory
WORKDIR /data

# Copy local configuration files to container
COPY owntone.conf /etc/owntone/owntone.conf

# Expose necessary ports
EXPOSE 3689 5000

# Start Owntone directly
ENTRYPOINT ["owntone", "-f", "-c", "/etc/owntone/owntone.conf"]
