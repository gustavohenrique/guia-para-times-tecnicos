# Política de Desenvolvimento de Software (PDS)

## 1. Introdução

A Política de Desenvolvimento de Software (PDS) aborda tópicos relacionados à segurança da informação voltados para um processo de desenvolvimento de software seguro.  
As diretrizes estabelecidas aqui não são obrigatórias, pois cada projeto tem suas particularidades, porém servem como um guia para um desenvolvimento focado em segurança da informação.

## 2. Autenticação de usuários

Autenticação de usuários é a funcionalidade mais comum em qualquer software que precise proteger informações particulares de pessoas não autorizadas. Também pode ser vista como uma vulnerabilidade a ser explorada através de técnicas como **ataque de força bruta**, **quebra de senha** e **engenharia social**.

- Não forneça mensagens de ajuda durante o procedimento de entrada (log-on) que poderiam auxiliar um usuário não autorizado;
- Bloqueie a conta do usuário e notifique-o quando houver muitas tentativas sem sucesso de entrada no sistema;
- Registre através de logs todas as tentativas de acesso ao sistema;
- Quando o procedimento de entrada no sistema finalizar com sucesso, mostre data e hora da última entrada no sistema e detalhes de qualquer tentativa sem sucesso de entrada no sistema desde o último acesso com sucesso;
- Não mostre a senha que está sendo informada;
- Não transmita senhas em texto puro pela rede;
- Encerre sessões inativas após um período definido de inatividade;
- Considere a utilização de Json Web Token (JWT) ou OAUTH2 para autenticação em APIs;
- Verifique a possibilidade de utilizar autenticação de dois fatores (2FA);
- Cuidado ao exigir apenas senhas fortes. Alguns usuários tendem a deixa-las anotadas em locais inseguros e isso pode ser pior do que utlizar uma senha fraca.

## 3. Bibliotecas de terceiros

Bibliotecas de terceiros são trechos de códigos desenvolvidos por pessoas de fora da organização que fornecem facilidades e recursos para quem as utiliza. Por exemplo, uma biblioteca existente para verificar se um número de CPF é válido evita que o desenvolvedor precise escrever um código apenas para isso.  
Cedo ou tarde todo software que precisa entregar valor rapidamente acaba utilizando uma ou várias bibliotecas.

- Crie um repositório privado para a organização ou o projeto e adicione as bibliotecas que você tenha certeza que não contêm vulnerabilidades ou código malicioso;
- Utilize ferramentas para fazer uma varredura nas bibliotecas em busca de vulnerabilidades, preferencialmente durante o processo de CI (Continuous Integration);
- Crie uma camada sobre as bibliotecas externas (encapsulamento) de modo que, caso seja necessário mudar de biblioteca, não precise alterar trechos de códigos espalhados.

## 4. Logs da aplicação

Logs são mensagens emitidas pelo software contendo pistas para ajuda a descobrir o que causou uma falha.

- Conte uma história através das mensagens e monte uma linha do tempo. Exemplo: "2018-01-31 11:47:50 Início do cadastro... 2018-01-31 11:47:51 Recebi uma requisição de cadastro para o email fulano@brainn.co. Vou verificar se já existe na base dados...";
- Não adicione informações sensíveis como senha e números de cartão de crédito;
- Restrinja o acesso ao logs apenas aos desenvolvedores e ao administrador do servidor;
- Utilize *datetime* completo;
- Forneça informações precisas que facilitem o entendimento em vez de mensagens confusas emitidas por algumas bibliotecas;
- Facilite o acesso aos logs para os desenvolvedores através de uma interface gráfica que permita visualizar e realizar buscas por determinadas palavras.

## 5. Ambientes de deploy

Todo website e software que roda na web fica hospedado em uma ou mais máquinas, também conhecidas como *ambientes*. Chamamos de ambiente de **produção** o conjunto de máquinas responsáveis por hospedar o software utilizado pelos usuários reais.  
É necessário testar o software antes de joga-lo em produção, em um ambiente com as configurações similares ao ambiente de produção, porém com informações que podem ser apagas sem problema. Esse ambiente é conhecido como **homologação** ou *staging* ou *QA (Quality Assurance)*.

- Crie um ambiente de **desenvolvimento** para testes dos desenvolvedores quando existirem profissionais de QA realizando testes no ambiente de homologação;
- Documente o procedimento para criar um novo ambiente similar ao de produção;
- Defina e documente as regras para a transferência de software entre ambientes. Exemplo: é necessária autorização do gerente para transferir de homologação para produção?
- Utilize um ambiente de teste para assegurar que mudanças em aplicações e sistemas operacionais, atualizações de segurança e correções de vulnerabilidades sejam testadas antes de serem aplicadas em produção;
- Organize e documente as permissões dos usuários para cada ambiente. Exemplo: desenvolvedores tem acesso de administrador em homologação e somente leitura de logs em produção;
- Informe visualmente quando o software está rodando em ambiente diferente de produção para evitar confusões. Exemplo: mudar o favicon em ambiente de homologação;
- Não copie dados sensíveis do ambiente de produção para outros ambientes;
- Coloque em variáveis de ambiente (ou secrets em caso de containers) as informações sensíveis utilizadas pelo software no ambiente de produção, e não no código fonte. Exemplo: senha do banco de dados;
- Documente os procedimentos necessários para executar o software em ambiente de produção.

## 6. DevOps e infraestrutura

DevOps é uma cultura cujo objetivo é possibilitar que o time de desenvolvimento consiga executar operações de infraestrutura, permitindo uma entrega mais ágil do software em produção.

- Automatize o deploy utilizando ferramentas open source de infraestrutura ágil existentes;
- Documente o processo de deploy automatizado;
- Configure um mecanismo que dê visibilidade para todo o time sobre quem executou o deploy, em qual data, em qual ambiente e qual versão do software;
- Utilize *containers* sempre que possível;
- Configure um mecanismo de monitoramento que envie uma alerta para o time informando sobre eventuais incidentes.

> Saiba como [contribuir](/CONTRIB.md)
