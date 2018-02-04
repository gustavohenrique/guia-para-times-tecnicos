# Como trabalhamos com Git

Na brainn.co utilizamos GitLab para projetos privados e Github para projetos públicos. Todas as informações abaixo se aplicam à ambos.

## Repositório

- Cada repositório deve ter uma descrição resumida do objetivo do projeto;
- Cada projeto deve ter seu próprio repositório e ciclo de deploy, sem interdependências;
- O repositório deve ter um `README.md` descrevendo seu objetivo, propósito, responsabilidades e dependências, bem como instruções de como configurar o ambiente de desenvolvimento e de produção, e como executar, testar e publicar o projeto;
- Deve haver apenas as branches `master` , `develop` , feature branches e hotfixes;
- Feature branches devem ser escritas como `feature/descricao_resumida` ;
- Bug fixes branches devem ser escritas como `hotfix/descricao_resumida` ;
- Mensagens de commit devem conter o título da task no card, explicação do motivo e link para o card;
- Mensagens de commit, texto no README e nomes de branches devem ficar em inglês.

## Configurações

O arquivo de configuração utilizado pelo Git é o `~/.gitconfig` . Segue um exemplo:

```
[user]
  name = Gustavo Henrique
  email = gustavo@brainn.co
[core]
  editor = vim
  whitespace = fix,-indent-with-non-tab,trailing-space,cr-at-eol
  excludesfile = ~/.gitignore
[push]
  default = matching
[pull]
  rebase = preserve
[branch]
  autosetuprebase = always
[color]
  ui = auto
[color "branch"]
  current = yellow bold
  local = green bold
  remote = cyan bold
[color "diff"]
  meta = yellow bold
  frag = magenta bold
  old = red bold
  new = green bold
  whitespace = red reverse
[color "status"]
  added = green bold
  changed = yellow bold
  untracked = red bold
[diff]
  tool = vimdiff
  compactionHeuristic = true
[difftool]
  prompt = false
[alias]
  a = add --all
  ai = add -i
  bd = branch -d
  ci = commit
  ca = commit -a
  cm = commit -m
  cam = commit -a -m
  cim = commit --amend
  l = log --oneline
  lg = log --oneline --graph --decorate
  me = merge
  co = checkout
  cob = checkout -b
  ps = push
  st = status
  tree = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
```

## Workflow

### Feature Branches:

Devem ser criados para novas funcionalidades ou modificações em funcionalidades existentes.

Criada a partir da: `develop`

O merge deve usar como destino: `develop`

Convenção do nome da branch: `feature/short-description-separated-by-hifen`

- Crie uma feature branch sempre a partir da `develop` :

    git checkout -b feature/add-login-form develop

- Escreva o código e faça um commit local usando um template de mensagem que deixa claro o que foi feito, o motivo e qual o card. O título deve iniciar com a letra maiúscula, escrito de forma imperativa e ter no máximo 50 caracteres:

```
Add a login form to authenticate users

https://trello.com/path/to/relevant/card

Users need to be authenticated before goes to the dashboard. The
authentication method is using JWT because it is a simple and secure
technology.

* Store the token in a localStorage
* Redirect to the dashboard after successfully logging
```

- Verifique se a branch `develop` possui atualizações remotas, faça um rebase para sua feature branch e resolva os conflitos que aparecerem:

```
git checkout develop
git pull origin develop
git checkout feature/add_login_form
git rebase develop
```

- Faça um push da feature branch e depois abra um `Merge Request` (GitLab) ou `Pull Request` (Github). As MR/PR que ainda não estiverem prontas para code review devem iniciar com o prefixo [WIP]. Se já finalizou a task ou story e a branch está apta para code review, junte todos os commits da branch em apenas um fazendo um rebase:

```
git rebase -i HEAD~X # sendo X o numero de commits
git push origin feature/add_login_form
```

- Quem aprovar o code review deve fazer o merge marcando a opção `remove source branch` .

### Hotfix Branches

Devem ser criadas para corrigir bugs em produção.

Criada a partir da: `tag`
O merge deve usar como destino: `develop` ou `master`
Convenção do nome da branch: `hotfix/short-description-separated-by-hyphen`

- Crie uma hotfix branch sempre a partir da tag que está em produção:

    git checkout -b hotfix/error-500-after-authentication v1.0.0

- Faça um commit como a correção e depois um push para submeter ao code review. Descreva na MR como reproduzir o bug, qual o resultado obtido e qual o esperado. Ou informe a URL do card que contenha essa descrição. Se a branch `develop` não sofreu alterações e está igual a `master` , então o Merge Request deve ser destinado à `develop` , senão para a `master` .

### Deploy

Pode ser feito o deploy da branch `develop` apenas para `staging` . Deve ser feito sempre que um Merge Request foi efetuado para ela.
O processo para deploy em `production` já é um pouco diferente. Ele inicia a partir do momento em que um MR da `develop` ou um `hotfix` é aprovado. Então, havendo a intenção de jogar o código em produção, primeiro deve ser criada uma tag utilizando o modelo de versionamento [SemVer](https://semver.org/) .

O deploy dessa tag deve ser feito primeiro em `staging` e após o QA ou PO testar e aprovar, então deve ser feito o deploy da mesma tag em `production` .
Nossa proposta inicial é utilizar o Jenkins para gerar automaticamente as tags e o changelog e gerenciar o deploy em `staging` e `production` fornecendo uma visão sobre quem executou o deploy, a data e qual a versão em cada ambiente.

## Fazendo Code Reviews

O processo de code-review tem sido uma prática comum nas empresas que prezam por mais qualidade no código. É essencial o olhar de outro desenvolvedor antes de um Merge Request ser aprovado.
Os comentários e discussões servem para estabelecer novos padrões, manter a qualidade do código, eliminar possíveis bugs e compartilhar conhecimento entre o time.
Acontece que, para que essas discussões sejam saudáveis, é necessário um pouco de empatia e seguir algumas práticas para tentar evitar comentários críticos destrutivos e humilhações:

### Revise apenas o necessário

Concentre-se em questões realmente importantes. Discussões sobre formatação do código e estilos devem ser evitadas. O time deve adotar uma ferrramenta de Linter para análise estática do código e utilizar [EditorConfig](http://editorconfig.org/) para exibir o código formatado de acordo com o gosto de cada no editor de textos.

### Todos devem participar da revisão

A responsabilidade não é exclusiva do mais sênior. Cada pessoa tem sua própria perspectiva sobre o código, podendo propor abordagens melhores em qualquer solução. Para que isso seja possível, todos devem buscar se familiarizar com o problema.

### Não se trata de avaliar pessoas

O feedback que o código recebe durante o Code Review não torna o desenvolvedor que escreveu o código bom ou ruim. O código que você escreve não te define.
Se você está revisando o código, não seja grosseiro em seu feedback. Mesmo que tudo esteja muito ruim, sempre há uma forma educada de comunicar isso.

### Utilize checklist

A utilização de checklist garante consistência durante o Code Review. Exemplo:

- O código está fácil de entender?
- Existe algum código de debug esquecido?
- O código respeita os princípios SOLID?
- Existe duplicação ou código redundante?
- O código está seguindo o padrão estrutural do projeto?
- As possíveis exceções estão sendo tratadas?
- Nomes de classes, métodos e variáveis estão coerentes?
- O código possui comentários desnecessários?
- Existe algum trecho incompleto?
- O código possui testes unitários e de integração suficientes?
- Os testes estão passando?
- Os testes unitários realmente testam o código?
- Os critérios de aceitação da story foram atendidos?

### Código bom ou ruim é uma questão de opinião

Bons desenvolvedores costumam ver o próprio código depois de algum tempo e perceber que podem melhorar. Não leve para o lado pessoal se você receber um feedback negativo do seu código. As críticas devem ser encaradas como sugestões de mudanças ou funcionar como base para uma discussão mais profunda que vai melhorar o entendimento entre os participantes.
Quando for avaliar e encontrar algum código bem escrito, não seja tímido, elogie seu companheiro. Feedbacks positivos ajudam na alto estima e a melhorar o relacionamento entre o time.

Code Review não deve ser encarado como um processo e sim como uma cultura.

> Veja como contribuir com os nossos Guias: ![/content/github.md](/content/img/github.svg)
