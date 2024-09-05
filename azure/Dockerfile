# Use the official Logstash image
FROM docker.elastic.co/logstash/logstash:8.11.0

# Copy the Logstash configuration file into the container
COPY logstash.conf /usr/share/logstash/pipeline/logstash.conf

# Change file permissions (switch to root user temporarily)
USER root
RUN chmod 644 /usr/share/logstash/pipeline/logstash.conf

# Switch back to the default user (non-root)
USER logstash