FROM node:24-bookworm-slim
WORKDIR /app
COPY app.tar.gz.b64 /tmp/app.tar.gz.b64
RUN base64 -d /tmp/app.tar.gz.b64 | tar -xz -C /app && rm /tmp/app.tar.gz.b64
ENV NODE_ENV=production
ENV PRAAT_DATA_DIR=/var/data/praat
EXPOSE 10000
CMD ["node", "bootstrap.mjs"]

