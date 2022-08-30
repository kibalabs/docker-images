FROM nginx:1.22.0

WORKDIR /app
COPY nginx.conf .
COPY start.sh .

EXPOSE 80
CMD ["./start.sh"]
