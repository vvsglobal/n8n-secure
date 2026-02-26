FROM node:20-bullseye-slim

# Use non-root user
RUN useradd -m n8nuser
USER n8nuser
WORKDIR /home/n8nuser

# Install Puppeteer + plugin + n8n
RUN npm install puppeteer puppeteer-extra puppeteer-extra-plugin-user-data-dir n8n

EXPOSE 5678

CMD ["n8n", "start", "--external", "--task-runner-mode=external"]
