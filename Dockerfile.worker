# Stage 1: get static ffmpeg binary (no package manager needed)
FROM mwader/static-ffmpeg:latest AS ffmpeg

# Stage 2: n8n with ffmpeg
FROM n8nio/n8n:latest

USER root
COPY --from=ffmpeg /ffmpeg /usr/local/bin/
COPY --from=ffmpeg /ffprobe /usr/local/bin/
USER node
