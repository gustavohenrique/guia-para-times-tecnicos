# Continuous Integration

Continuous Integration (CI), ou integração contínua, é uma prática de desenvolvimento de software onde os membros da equipe integram seu trabalho. Cada integração é verificada por uma ferramenta de build automatizado (incluindo testes, taxa de cobertura, estilo e padrões de código) com a finalidade de detectar erros de integração o mais rápido possível, economizando assim o custo de correção nas fases posteriores do projeto, que é muito mais alto.
Os passos executados em CI são:

1. Clone do código fonte
1. Análise estática do código (linter)
1. Execução dos testes automatizados
1. Relatório de cobertura de testes
1. Notificação do sucesso ou falha do CI

## Ferramentas:

- GitLab-CI: Integrado ao GitLab
- Travis-CI: Integrado ao Github
- Jenkins: É um fork open source do projeto Hudson, criado após a Oracle ter comprado a Sun Microsystems e exigir mudanças na licença do projeto. Desenvolvedores insatisfeitos com a postura da Oracle em relação ao Hudson resolveram seguir separado. Jenkins possui integração com diversas outras ferramentas e é bem extensível com o uso de plugins.

> Saiba como [contribuir](/CONTRIB.md)
