# Use official n8n image as base (includes n8n, Node.js, Chromium)
FROM n8nio/n8n:latest

# Switch to root to install Puppeteer plugins
USER root

# Install Puppeteer Extra and plugins
RUN npm install --no-save \
    puppeteer-extra \
    puppeteer-extra-plugin-stealth \
    puppeteer-extra-plugin-user-data-dir

# Switch back to n8n user
USER node

# Expose default n8n port
EXPOSE 5678

# Start n8n in external task runner mode
CMD ["n8n", "start", "--tunnel", "--task-runner-mode=external"]
