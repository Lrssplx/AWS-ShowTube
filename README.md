# ShowTube
Trabalho Final da disciplina Trabalho individual em Arquitetura de Computadores. Tendo como tema programação em nuvem.

A aplicação consiste em um clone do youtube (ShowTube), onde os usuários podem fazer upload, download, remover e assistir vídeos. Foi utilizado provedor Lambda da AWS para que o foco estivesse apenas na aplicação sem se preocupar com servidor. Na conta AWS criou-se um novo usuário e uma nova política, já para usar o serverless utilizou-se o NodeJS. Funcionalidades consistem em:

- Upload de um vídeo: O usuário faz o upload pela interface web e o vídeo é salvo diretamente no Serviço S3;
- Listar vídeos disponíveis: A interface web manda uma requisição de listagem para o serviço API Gateway e a requisição é enviada para a função List no Lambda. Essa função vai buscar todos os vídeos disponíveis no S3 e retornar uma lista;
- Remover um vídeo: A interface web manda uma requisição de remoção de um vídeo para o serviço API Gateway e a requisição é enviada para a função Delete no Lambda. Essa função vai remover o vídeo do S3.

