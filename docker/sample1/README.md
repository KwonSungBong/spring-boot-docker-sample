# ngins ssl spring boot


https://github.com/Valian/docker-nginx-auto-ssl


docker run -d \
  --name nginx-auto-ssl \
  --restart on-failure \
  -p 80:80 \
  -p 443:443 \
  -e ALLOWED_DOMAINS=bookstorage.kr \
  -e SITES='bookstorage.kr=localhost:8080;*.bookstorage.kr=localhost:8080' \
  valian/docker-nginx-auto-ssl


docker run -d \
  --name nginx-auto-ssl \
  --restart on-failure \
  -p 80:80 \
  -p 443:443 \
  -e ALLOWED_DOMAINS=bookstorage.kr \
  -e SITES='bookstorage.kr=localhost:8080;*.bookstorage.kr=localhost:8080' \
  -e DIFFIE_HELLMAN=true \
  -v ssl-data:/etc/resty-auto-ssl \
  valian/docker-nginx-auto-ssl



