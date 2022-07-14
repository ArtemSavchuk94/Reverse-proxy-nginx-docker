# Reverse-proxy-nginx-docker
Docker compose exec public bash
Copy /etc/nginx/conf.d file
ADD location /api {
      rewrite /api /$1 break;
      proxy_pass http://devops-be:3000/;
    }
Volume:    ./nginx/conf.d:/etc/nginx/conf.d
