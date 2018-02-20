# Metodologia de Projetos

## Introdução

Na brainn, utilizamos métodos e princípios ágeis para geração do máximo valor para os stakeholders dos nossos projetos. Praticamos o Scrum em projetos de escopo flexível, permitindo que os valores do [Manifesto Ágil](http://agilemanifesto.org/) sejam respeitados no dia-a-dia, por meio de papéis, artefatos e cerimônias praticados pelos nossos squads.

A visão do fluxo detalhado de uma Sprint pode ser visualizada pelos membros do nosso time por meio deste [arquivo UML](https://www.lucidchart.com/documents/edit/829755ad-dbfb-4514-bc5a-308a02628e0e).

## 1) Story Time

Um passo que muitas vezes é relegado à Planning é a estimação dos Pontos das Estórias de uma determinada Release de um produto. É uma atividade de background que demanda algum tempo recorrente (e.g., 1 hora por semana), mas que traz um valor enorme aos squads do projeto. Exemplos de benefícios:

- Auxilia na priorização do Product Backlog pelo Product Owner
- Ajuda o squad a estimar quando a release poderá ser lançada ao mercado
- É um exercício que ajuda o squad a antever futuras Sprints, mudando decisões na atual
- Explicita deficiências do Product Backlog antes da Planning, dando tempo para refinamento
- Indica ao Product Owner quando uma Estória precisa ser quebrada em partes menores

As Estórias têm pesos associados pelo squad por meio de Pontos, que é uma medida relativa de esforço e risco, ou seja, pode-se usar uma medida arbitrária contato que exista consistência do peso utilizado para as Estórias ao longo das Sprints (e.g., uma Estória de 2 pontos de uma Sprint deve representar o dobro de dificuldade em relação a uma Estória de 1 ponto de qualquer Sprint).

Deve-se sair do exercício com os Critérios de Aceitação (também chamados de Condições de Satisfação) das Estórias muito bem definidos, justamente porque os mesmos dão fundamento básico às estimativas de Pontos dadas pelo squad.

>**DICA:** Algumas [práticas ruins](https://medium.com/bynder-tech/12-common-mistakes-made-when-using-story-points-f0bb9212d2f7) devem ser evitadas:
- Não usar referências históricas para o peso relativo de Estórias
- Dar pontos para Tasks ao invés de utilizar a estimativa para Estórias em função de...
- ...Não quebrar Estórias maiores (Épicos) em Estórias menores, mais fáceis de serem implementadas
- Não elucidar uma Estória quando diferentes membros do squad dão estimativas muito díspares
- Ajustar os Pontos estimados ao longo da Sprint ao invés de discutir isso na Retrospectiva
- [Associar Pontos com Tasks](https://www.mountaingoatsoftware.com/blog/dont-estimate-the-sprint-backlog-using-task-points), que são difíceis de comparar, quando o interesse na verdade é mapear gargalos no fluxo da execução ao longo da Sprint

Nada impede que o Product Owner valide posteriormente eventuais dúvidas apresentadas no exercício e que requerem uma pesquisa mais aprofundada, o que poderá por sua vez alterar a estimativa coletiva no futuro.

Na realidade, a função do Product Owner é diariamente realizar [aprofundamentos sobre a UX](https://uxchecklist.github.io/), decidindo com os stakeholders o que o produto deve conseguir fazer primeiro e realizar dinâmicas de User Story Mapping constantemente ao longo das Sprints.

> **DICA:** A pior coisa que pode acontecer a um Product Owner é ficar estrito a documentação de Estórias. Sua curiosidade e poder de convencimento deve também levar os stakeholders a se convencerem que as suas sugestões fazem sentido. A comprovação pode ser simplesmente subjetiva como baseada em dados primários ou secundários. Se houver Tasks que o time tenha que executar para refutar uma determinada hipótese, essa deve entrar no Product Backlog.

## 2) Sprint Planning

**(a) Definir o Backlog da Sprint**

O Product Owner lidera a discussão, apresentando o Product Backlog atualizado e identificando as Estórias que foram priorizadas por meio de técnicas de associação de Valor de Negócios, explicando o Contexto e os Critérios de Aceitação de cada uma delas.

O envolvimento e a discussão sobre os detalhes de cada Estória pelo time devem ser incentivados para que o entendimento dos objetivos seja realmente compartilhado por todos e não ocorra o problema do trabalho desperdiçado em função de um entendimento falho ou parcial do que deveria ser entregue.

Apesar do Product Owner definir a prioridade das Estórias, quem determina quantas serão entregues na Sprint é o squad. As Estórias selecionadas para a Sprint representam o Backlog da Sprint.

As Estórias, quando escolhidas para integrar o Backlog da Sprint, passa para o status Commited.

**(b) Definir Tasks**

O squad discute, uma Estória por vez, tudo o que precisa ser feito para que aquela Estória seja de fato considerada entregue (as Tasks). Exemplos: fazer uma pesquisa com usuários, desenhar telas, ajustar uma base de dados, configurar uma nova configuração no servidor, pesquisar uma determinada lib, documentar o FAQ, etc.

O ideal é que Tasks sejam granulares o suficiente para que seja fácil realizar o tracking ao longo da Sprint. Algumas ferramentas, como o ZenHub, permitem relacionar Tasks à Estórias e a criar uma hierarquia de dependências entre as mesmas, facilitando a execução do caminho crítico.

Uma convenção que pode ser utilizada é não criar Tasks que demorem mais que 4 horas (meio dia útil) para serem finalizadas. A palavra final sobre essa estimativa sobre a duração é de quem vai realizar a Task, ao contrário dos Pontos das Estórias, que é uma medida coletiva.

É um exercício criativo e que precisa ser concluído com o entendimento claro do que precisa ser feito pelo time ao longo das duas ou mais semanas da Sprint.

Ao longo da Sprint, novas Estórias ou Tasks poderão ser adicionadas ao Backlog da Sprint se houver consentimento do time, o que é chamado de Scope Change. Isso deverá ser tratado na Daily.

Quando todas as Tasks forem criadas, a Estória passa para o status Ready.

> **DICA:** Para uma Estória ser considerada Ready e o time de fato ter uma visibilidade horizontal, é recomendado que discutam de forma explícita:
- Critérios de Aceitação da Estória
- Roteiro de Testes (funcionais ou não)
- Acordo informal sobre o fluxo de trabalho da Sprint
- [User Flows](https://www.smashingmagazine.com/2012/01/stop-designing-pages-start-designing-flows/) que serão alterados e/ou criados
- [Requerimentos de Arquitetura da Informação](http://alistapart.com/article/thedisciplineofcontentstrategy)
- [Análise de Dados](https://uxdesign.cc/ux-tools-for-analytics-and-metrics-51634c3c26ec) que serão implementados
- Validação de Hipóteses (e.g., [Diamante Duplo](https://brasil.uxdesign.cc/ux-design-toolbox-ced4b7f209d0))
- Necessidade de documentação para usuários

Ao longo da Sprint, todos os stakeholders devem ter visibilidade completa sobre a Board, ajudando a identificar oportunidades de melhorias e gargalos. O time deve estar sincronizado e preferencialmente utilizando ferramentas que se adequem ao seu processo, e não o inverso.

> **DICA:** Gostamos de usar o GitHub em conjunto com o [ZenHub](https://medium.com/@ZenHub/how-to-use-github-for-agile-project-management-2c5b0ec1dad6), um plugin para times ágeis gerirem seu Product Backlog de forma integrada. Ele extrai algumas métricas de forma automática, sem esforço adicional. Para métricas mais avançadas, há um projeto [open source](https://github.com/Adphorus/zenhub-charts) que permite importar ainda mais informações do mesmo sistema.

## 3) Daily

A Daily é um encontro rápido (10 a 15 minutos), presencial e/ou virtual, diário, e liderado pelo Scrum Master. Visa a comunicação síncrona do time, por isso recomenda-se que não se torne um exercício mecânico de simples status update, pois essa é uma prática não ágil. E também deve-se evitar bots de Daily, pois esses incentivam o exercício mecânico e torna um exercício focado na documentação, e perde-se o foco de criar uma verdadeira colaboração e interesse mútuo entre o trabalho dos membros do squad.

A pauta clássica para o que cada um deve informar para os demais do squad:

- O que foi feito desde a última Daily
- O que pretende fazer até a próxima Daily
- Qual ajuda precisará para realizar a sua entrega

Ao término da Daily, o Scrum Master sai com uma lista de to-do para ajudar o time a se tornar mais produtivo, retirando os impeditivos.

>**DICA:** A melhor forma de fazer com que a Daily não se torne mecânica é respeitar os 4 Valores Ágeis:
1. Todos devem se comunicar de forma proativa e as opiniões devem ser respeitadas
2. O foco deve ser a visibilidade, e não na documentação do que foi feito ou não feito
3. Deve haver a colaboração e o ownership do time sobre o que está sendo realizado na Sprint
4. Reagir a mudança para gerar valor de fato, ao invés de obedecer o plano original da Sprint

> Inclusive, na Daily o time pode tomar decisões de alterar, aumentar ou reduzir o escopo da Sprint, e isso ser traduzido como um Scope Change

## 4) Review

Na Review, o squad irá mostrar o software criado ao longo das últimas semanas para todos os stakeholders. A demonstração deve levar cerca de meia hora a uma hora por semana de Sprint.

Independente de ser a primeira ou a última Sprint de uma determinada Release, sempre há o que ser demonstrado, pois os loops de feedback devem sempre ocorrer em um time ágil.

Cada Estória apresentada deve cumprir os Critérios de Aceitação e deve ter passado com sucesso nos Testes.

As Estórias não finalizadas devem ser apresentadas e os feedbacks obtidos dos stakeholders devem ser incorporados pelo squad. Em muitos casos, há uma tendência natural de querer discutir o que será realizado na próxima Sprint, mas essa é uma matéria da Planning e não da Sprint Review.

> **DICA:** Muitos times praticam o pré-Review, que é um momento ainda sem a participação de todos os stakeholders, onde o Product Owner realiza o QA funcional ao vivo na frente do time. É uma boa prática, pois melhora a capacidade de se apresentar o valor criado pelo time e discute-se novas formas de se realizar a demonstração pública.

## 5) Retrospectiva

Na Retrospectiva, o squad deve analisar métricas e opiniões qualitativas para priorizar e decidir alterações internas do time. É uma cerimônia que procura atingir o objetivo da melhoria contínua do time, identificando e retirando potenciais gargalos, e compartilhando aprendizados com as demais equipes.

O primeiro passo é a análise das métricas ágeis que o squad está mapeando na sua Sprint, incluindo o Velocity, Release Report, Burndown, Cycle Analysis, entre outros.

Com a análise de métricas, o time deve propor, de forma democrática (i.e., há diversos exercícios que se propõem a incentivar a participação de todos) o que não funcionou na Sprint e precisa ser melhorado. Deve haver sempre uma priorização, pois trata-se de uma melhoria de processo de forma incremental, ágil, e não radical.

Também são discutidas se as melhorias propostas nas Retrospectivas anteriores levaram a algum impacto positivo e se o time decide continuar praticando as mesmas nas futuras Sprints.

>**DICA:** Depois de discutidas e agrupadas as propostas pelos times, deve-se decidir por implementar poucos temas estratégicos (e.g., 2 iniciativas mais votadas). Também deve-se mapear inicialmente poucas métricas, pois elas por si só geram informações valiosas. Depois de exauridas as melhorias sobre as métricas mais tradicionais, o time pode buscar métricas mais avançadas, como por exemplo aquelas de [código fonte](https://www.gitprime.com/product/).
