# Simple static site served by Nginx
FROM nginx:alpine

# Use your nginx.conf in the repo (already present)
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy site files (index.html, main.js, etc.)
COPY . /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
