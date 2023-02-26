FROM nginx:1.23.3

WORKDIR /app
COPY nginx.conf .
COPY start.sh .

EXPOSE 80
CMD ["./start.sh"]
