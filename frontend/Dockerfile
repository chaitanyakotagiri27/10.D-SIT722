FROM nginx:alpine
# use your repo's nginx config and static files
COPY ./frontend/nginx.conf /etc/nginx/conf.d/default.conf
COPY ./frontend/ /usr/share/nginx/html
EXPOSE 80
CMD ["nginx","-g","daemon off;"]
