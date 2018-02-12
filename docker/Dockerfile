# Build from nginx folder with:
# docker build -t tbnginx -f docker/run/Dockerfile .

# Run with
# docker stop tbnginx && docker rm tbnginx && docker run --name tbnginx -d -p 80:80 tbnginx

FROM nginx

# Copy relevant nginx files
COPY nginx.conf /etc/nginx/nginx.conf
COPY sites-available /etc/nginx/sites-available
COPY sites-enabled /etc/nginx/sites-enabled

# Copy static files for health check
COPY ./health-check/ /usr/share/nginx/health-check

