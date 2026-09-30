Nome: Luis Felipe Cardoso
RA:FO352a9b57c8aa4c9492

## O que fiz
Executei uma página web em um container Docker chamado estoque.
Usei a imagem nginx:alpine e a porta 8085 do ambiente.

## Verificação do conteiner

cole aqui a saida do comando docker ps:
docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                     NAMES
c674ff260bd6   nginx:alpine   "/docker-entrypoint.…"   53 seconds ago   Up 52 seconds   0.0.0.0:8085->80/tcp, [::]:8085->80/tcp   estoque

## Teste da pagina

cole aqui a resposta do comando curl http://localhost:8085:
curl http://localhost:8085
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
com minhas palavras, qual é a diferença entre a imagem ngix:alpine e o container estoque? para que serviu o mapeamento 8085:80
R: A diferença principal é que nginx:alpine é o modelo (a imagem) e o estoque é a aplicação prática desse modelo em execução (o contentor).
O mapeamento 8085:80 serve para redirecionar o tráfego da sua máquina física para dentro do contentor permitindo aceder à aplicação através do  navegador.
