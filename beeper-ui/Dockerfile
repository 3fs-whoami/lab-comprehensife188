FROM registry.ocp4.example.com:8443/ubi8/nodejs-16:1 as builder
WORKDIR /opt/app-root/src
USER root
COPY . .
RUN npm install && \
    npm run build

FROM registry.ocp4.example.com:8443/ubi8/nginx-118:1
COPY nginx.conf /etc/nginx
COPY --from=builder /opt/app-root/src/build/ /usr/share/nginx/html
CMD nginx -g "daemon off;"
