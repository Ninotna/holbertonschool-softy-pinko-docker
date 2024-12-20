# Use the latest version of Nginx as the base image
FROM nginx:latest

# Copy the front-end files into the Nginx default directory
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the custom Nginx configuration file
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose port 9000 (recommended port to access the site)
EXPOSE 9000

# Nginx will run automatically, so no need for CMD (Nginx starts by default)
