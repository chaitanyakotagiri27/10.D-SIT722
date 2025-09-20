FROM nginx:alpine
# Paths are relative to the build context (./frontend), so no "frontend/" prefix
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY . /usr/share/nginx/html
EXPOSE 80
CMD ["nginx","-g","daemon off;"]
