FROM nginx:1.21.6

WORKDIR /app
COPY nginx.conf .
COPY start.sh .

EXPOSE 80
CMD ["./start.sh"]
