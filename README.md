# Projeto Docker e PostgreSQL

Desenvolvi um projeto para criar do zero um ambiente de trabalho usando o Docker e o PostgreSQL. Primeiro, configurei um "container" (um ambiente isolado onde os programas podem rodar) 
no Docker e utilizei uma "imagem" do PostgreSQL, que funciona como uma base pré-configurada do sistema de banco de dados.

Dentro desse ambiente, configurei um banco de dados, definindo quem poderia acessá-lo (usuários), quais informações ele deveria armazenar (tabelas) e como os dados seriam organizados 
(schemas). Por fim, fiz testes ao realizar algumas consultas no banco, para garantir que tudo estava funcionando corretamente.

O objetivo principal foi construir esse ambiente do zero, como forma de praticar e aprofundar meus conhecimentos em ferramentas de orquestração e bancos de dados.

<div align="center">
  <img src="https://github.com/CamilaDeAlm/Projeto-PostgreSQL-e-Docker/blob/main/folder/Captura%20de%20tela%202025-01-06%20151314.png" alt="Exemplo" width="largura" height="altura">
</div>

## Execução Docker:

docker run --name camila -p 5434:5432 -e POSTGRES_USER=camila -e POSTGRES_PASSWORD=123 -e POSTGRES_DB=camila -d postgres:16.0

## Consultas básicas:

SELECT id, nome, sobrenome, nota_exame1, nota_exame2, tipo_sistema_operacional

FROM camila.teste;

<div align="center">
  <img src="https://github.com/CamilaDeAlm/Projeto-PostgreSQL-e-Docker/blob/main/folder/Captura%20de%20tela%202025-01-06%20152445.png" alt="Exemplo" width="largura" height="altura">
</div>


SELECT id, nome, sobrenome, nota_exame1, nota_exame2, tipo_sistema_operacional

FROM camila.teste

ORDER BY tipo_sistema_operacional DESC, nome ASC;

<div align="center">
  <img src="https://github.com/CamilaDeAlm/Projeto-PostgreSQL-e-Docker/blob/main/folder/Captura%20de%20tela%202025-01-06%20152310.png" alt="Exemplo" width="largura" height="altura">
</div>

Fim.

