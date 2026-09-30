# Prova-Computa-o-em-Nuvem

root@ubuntu:~$ cat>index.html<<'EOF'
> <!DOCTYPE html>
> <html lang="pt-BR">
> <head>
> <meta charset="UTF-8">
> <title>Estoque</title>
> </head>
> </bodi>
> <h1>Estoque disponivel<h1>
> </body>
> </html>
> EOF
root@ubuntu:~$ docker run -d --name estoque -p 8085:80 nginx:alpine
Unable to find image 'nginx:alpine' locally
alpine: Pulling from library/nginx
e2de96513ba9: Pull complete 
d9aae54b5831: Pull complete 
6c53d0b2a666: Pull complete 
745dfb2690dd: Pull complete 
9a9a644fdd6a: Pull complete 
64c8194480fe: Pull complete 
e76228b47809: Pull complete 
e72112c14215: Pull complete 
Digest: sha256:df221db836e1754089190208cee7eeda94f233197056426eda74a43ab1abeac2
Status: Downloaded newer image for nginx:alpine
c674ff260bd60730adc81f8b2b4ecd597c4b54f0b7e0e246cd45dd867d972e2f
root@ubuntu:~$ docker cp index.html estoque:/usr/share/nginx/html/index.html
Successfully copied 2.05kB to estoque:/usr/share/nginx/html/index.html
root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                     NAMES
c674ff260bd6   nginx:alpine   "/docker-entrypoint.…"   53 seconds ago   Up 52 seconds   0.0.0.0:8085->80/tcp, [::]:8085->80/tcp   estoque
root@ubuntu:~$ curl http://localhost:8085
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Estoque</title>
</head>
</bodi>
<h1>Estoque disponivel<h1>
</body>
</html>
