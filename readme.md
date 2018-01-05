
# Docker nginx example

#### Example usage
This nginx container will forward requests to port 80 to port 8001

```
docker run -d \
  --name nginx-test
  -p 80:80 \
  -p 443:443 \
  --net="host" \
  -v /path/to/your/nginx.conf:/etc/nginx/nginx.conf:ro \
  --restart always \
  nginx
```