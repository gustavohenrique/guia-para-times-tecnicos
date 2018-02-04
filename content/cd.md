# Continuous Delivery vs. Continuous Deployment

## Continuous Delivery

Continuous Delivery (CD), ou Entrega Contínua, é um conjunto de práticas que tem como objetivo garantir que o novo código pode ser implantado em algum servidor a qualquer momento. 

Na prática de entrega contínua tratamos do envio do código para um ambiente, que pode ser DEV, STAGE ou PROD, uma vez que o desenvolvedor sente o código está pronto para enviar. Mas nesta parte do processo a idéia é de que se está entregando o código para um conjunto de usuários poderem testar o software.

## Continuous Deployment

Continuous Deployment, ou Implantação Contínua, difere do processo de Continuous Delivery ao permitir entregar o software em ambiente de produção tão logo você esteja certo de que o código passou por todos os testes e está pronto para ser publicado. A idéia é entregar valor de negócio o mais rápido possível e não acumular código novo em stage. Ou seja, se o código passou pelo processo de integração que é responsável por testes de integração ou testes unitários, e também foi avançando no processo de delivery com testes manuais, visuais e de comportamento, então entra a fase de deployment que é responsável por publicar o código em produção de forma automatizada.

Nesta fase do processo assume-se que todos os testes foram feitos, e apenas será tratada a questão de publicação automatizada no ambiente de produção.

Parte-se do princípio de que o ambiente de produção é estável, de que tudo foi testado e que este processo deverá ser simples como apertar um botão e que deverá ser possível de ser feito por qualquer pessoa.

Ou seja, para Continuous Deployment, você necessariamente precisa ter Continuous Integration e Continuous Delivery funcionando como parte da sua rotina.

## Ferramentas

Não existem ferramentas específicas para esse tipo de entrega. Geralmente são utilizadas as mesmas ferramentas de Continuous Integration apenas executando outros comandos para permitir fazer o deploy, entregar o software, nos servidores. Esses comandos variam de acordo com as tecnologias envolvidas como linguagem de programação, framework e configurações do servidor.