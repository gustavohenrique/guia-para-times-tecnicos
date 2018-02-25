# Metodologia de Projetos

## Introdução

Na brainn, utilizamos métodos e princípios ágeis para geração do máximo valor para os stakeholders dos nossos projetos. Praticamos o Scrum em projetos de escopo flexível, permitindo que os valores do [Manifesto Ágil](http://agilemanifesto.org/) sejam respeitados no dia-a-dia, por meio de papéis, artefatos e cerimônias praticados pelos nossos Squads.

## Papéis

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad em cada uma das cerimônias listadas a seguir. Para uma visão mais detalhada, recomendamos a leitura do [Perfil Brainner](/content/brainner.md).

## Cerimônias

A visão do fluxo detalhado de uma Sprint pode ser melhor visualizada pelos membros do nosso time por meio deste [fluxograma](https://www.lucidchart.com/documents/edit/829755ad-dbfb-4514-bc5a-308a02628e0e).

#### 1) Grooming

Um passo que muitas vezes é relegado à Planning é a estimação dos Pontos das Estórias de uma determinada Release de um produto. É uma atividade de background que demanda algum tempo recorrente (e.g., 1 hora por semana), mas que traz um valor enorme aos Squads do projeto. Exemplos de benefícios:

- Permite uma previsão de lançamento de uma Release em desenvolvimento (Release Report)
- Auxilia na priorização das Estórias pelo Product Owner se comparado com o Valor de Negócio
- Permite o Squad a tomar decisões mais bem informadas em relação a futuras Estórias da Release
- Explicita deficiências de entendimento em relação ao Backlog do Produto antes de uma Planning
- Indica ao Product Owner quando uma Estória está muito complexa e precisa ser quebrada

As Estórias têm pesos associados pelo Squad por meio de Pontos das Estórias, que é uma medida relativa de esforço e risco, ou seja, pode-se usar uma medida arbitrária contato que exista consistência do peso utilizado para as Estórias ao longo das Sprints (e.g., uma Estória de 2 pontos de uma Sprint deve representar o dobro de dificuldade em relação a uma Estória de 1 ponto de qualquer Sprint, passada ou atual).

Deve-se sair do exercício com os Critérios de Aceitação (também chamados de Condições de Satisfação) das Estórias, justamente porque os mesmos dão fundamento às estimativas de Pontos das Estórias dadas pelo Squad.

>**DICA:** Alguns [erros](https://medium.com/bynder-tech/12-common-mistakes-made-when-using-story-points-f0bb9212d2f7) devem ser evitados:
- Não usar as referências históricas para o peso relativo de Estórias
- Não quebrar Estórias em Estórias menores, mais granulares e fáceis de observar no Burndown
- [Associar pontos com Tasks](https://www.mountaingoatsoftware.com/blog/dont-estimate-the-sprint-backlog-using-task-points),  quando a verdadeira intenção é mapear gargalos nos fluxos das Tasks
- Não aprofundar o entendimento de uma Estória quando diferentes membros do Squad dão estimativas muito díspares
- Modificar os Pontos das Estórias ao longo da Sprint ao invés de discutir isso com o Squad na Retrospectiva

Nada impede que o Product Owner valide posteriormente eventuais dúvidas que surgiram no Grooming e que requerem uma pesquisa mais aprofundada, o que poderá por sua vez alterar a estimativa dos Pontos da Estória no próximo Grooming ou na Planning.

Na realidade, a função do Product Owner é diariamente melhorar o seu [entendimento sobre a UX](https://uxchecklist.github.io/), decidindo com os stakeholders o que o produto deve conseguir fazer primeiro, executando dinâmicas de User Story Mapping constantemente ao longo das Sprints.

> **DICA:** A pior coisa que pode acontecer a um Product Owner é ficar estrito a documentação de Estórias. Sua curiosidade e poder de convencimento deve também levar os stakeholders a se convencerem que as suas sugestões fazem sentido. A comprovação pode ser simplesmente subjetiva como baseada em dados primários ou secundários. Se houver Tasks que o time tenha que executar para refutar uma determinada hipótese, essa deve entrar no Backlog do Produto.

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e o Backlog do Produto seja atualizado|
|Product Owner|Antes do Grooming, documentar os objetivos, valor de negócio, usuários envolvidos, sketches, benchmark, e os critérios de aceitação das Estórias da Release atual|
|Squad|Estimar o esforço para a entrega das Estórias utilizando como referência outras Estórias já entregues, indicando quando uma Estória precisar ser quebrada|
|Squad|Indicar se houver risco técnico ou de segurança relacionado a uma Estória, indicando alternativas ou validações por meio de POC|

#### 2) Sprint Planning

**(a) Definir o Backlog da Sprint**

O Product Owner lidera a discussão, apresentando o Backlog do Produto atualizado e identificando as Estórias que foram priorizadas por meio de técnicas de associação de Valor de Negócios, explicando o Contexto e os Critérios de Aceitação de cada uma delas.

O envolvimento e a discussão sobre os detalhes de cada Estória pelo time devem ser incentivados para que o entendimento dos objetivos seja realmente compartilhado por todos e não ocorra o problema do trabalho desperdiçado em função de um entendimento falho ou parcial do que deveria ser entregue.

Apesar do Product Owner definir a prioridade das Estórias, quem determina quantas serão entregues na Sprint é o Squad. As Estórias selecionadas para a Sprint representam o Backlog da Sprint.

As Estórias, quando escolhidas para integrar o Backlog da Sprint, passa para o status Commited.

**(b) Definir Tasks**

O Squad discute, uma Estória por vez, tudo o que precisa ser feito para que aquela Estória seja de fato considerada entregue (as Tasks). Exemplos: fazer uma pesquisa com usuários, desenhar telas, ajustar uma base de dados, configurar uma nova configuração no servidor, pesquisar uma determinada lib, documentar o FAQ, etc.

O ideal é que Tasks sejam granulares o suficiente para que seja fácil realizar o tracking ao longo da Sprint. Algumas ferramentas, como o ZenHub, permitem relacionar Tasks à Estórias e a criar uma hierarquia de dependências entre as mesmas, facilitando a execução do caminho crítico.

Uma convenção que pode ser utilizada é não criar Tasks que demorem mais que 8 horas (dia útil) para serem finalizadas. A palavra final sobre essa estimativa sobre a duração é de quem vai realizar a Task, ao contrário dos Pontos das Estórias, que é uma medida coletiva.

É um exercício criativo e que precisa ser concluído com o entendimento claro do que precisa ser feito pelo time ao longo das duas ou mais semanas da Sprint.

Ao longo da Sprint, novas Estórias ou Tasks poderão ser adicionadas ao Backlog da Sprint se houver consentimento do time, o que é chamado de Scope Change. Isso deverá ser tratado na Daily.

Quando todas as Tasks forem criadas, a Estória passa para o status Ready.

> **DICA:** Para uma Estória ser considerada Ready e o time de fato ter o entendimento compartilhado, é recomendado que o Squad discuta:
- Critérios de Aceitação
- Roteiros de Testes
- Definition of Done
- Sequência de Tasks
- Mudanças nos [User Flows](https://www.smashingmagazine.com/2012/01/stop-designing-pages-start-designing-flows/)
- Revisão da [Arquitetura da Informação](http://alistapart.com/article/thedisciplineofcontentstrategy)
- Ativação de [Métricas](https://uxdesign.cc/ux-tools-for-analytics-and-metrics-51634c3c26ec)
- Validação de Hipóteses (e.g., [Diamante Duplo](https://brasil.uxdesign.cc/ux-design-toolbox-ced4b7f209d0))
- Necessidade de documentação para usuários

Ao longo da Sprint, todos os stakeholders devem ter visibilidade completa sobre o Backlog da Sprint, ajudando a todos identificarem oportunidades de melhorias e gargalos. O uso de ferramentas deve responder ao processo decidido pelo time e não o inverso. A extração de métricas deve ser o mais automatizada possível para não gerar trabalho adicional para o Squad e ser voltada para o objetivo de melhoria contínua e não para a simples cobrança por produção.

> **DICA:** Gostamos de usar o GitHub em conjunto com o [ZenHub](https://medium.com/@ZenHub/how-to-use-github-for-agile-project-management-2c5b0ec1dad6), um plugin para times ágeis gerirem seu Backlog do Produto de forma integrada. Ele extrai algumas métricas de forma automática, sem esforço adicional. Para métricas mais avançadas, há um projeto [open source](https://github.com/Adphorus/zenhub-charts) que permite importar ainda mais informações do mesmo sistema.

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e o Backlog da Sprint seja atualizado|
|Product Owner|Antes da Planning, decidir quais Estórias do Backlog do Produto serão priorizadas para o desenvolvimento|
|Squad|De forma sequencial, confirmar os Pontos das Estórias que foram puxadas para a próxima Sprint|
|Squad|Contribuir com o cumprimento do checklist para a Estória estar Ready para desenvolvimento|
|Squad|Decidir quantas Estórias serão incorporadas no Backlog da Sprint|

#### 3) Daily

A Daily é um encontro rápido (10 a 15 minutos), presencial e/ou virtual, diário, e liderado pelo Scrum Master. Visa a comunicação síncrona do time, por isso recomenda-se que não se torne um exercício mecânico de simples status update, pois essa é uma prática não ágil. E também deve-se evitar bots de Daily, pois esses incentivam o exercício mecânico e torna um exercício focado na documentação, e perde-se o foco de criar uma verdadeira colaboração e interesse mútuo entre o trabalho dos membros do Squad.

A pauta clássica para o que cada um deve informar para os demais do Squad:

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

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e o Backlog da Sprint seja atualizado|
|Squad|Comunicar com o time sobre o andamento das Tasks e desafios encontrados|
|Product Owner|Indicar eventuais bugs críticos (C0 ou C1) que tenham surgido no QA|
|Squad|Alterar o escopo do Backlog da Sprint, em casos extremos ("Scope Change")|

#### 4) Review

Na Review, o Squad irá mostrar o software criado ao longo das últimas semanas para todos os stakeholders. A demonstração deve levar cerca de meia hora a uma hora por semana de Sprint.

Independente de ser a primeira ou a última Sprint de uma determinada Release, sempre há o que ser demonstrado, pois os loops de feedback devem sempre ocorrer em um time ágil.

Cada Estória apresentada deve cumprir os Critérios de Aceitação e deve ter passado com sucesso nos Testes.

As Estórias não finalizadas devem ser apresentadas e os feedbacks obtidos dos stakeholders devem ser incorporados pelo Squad. Em muitos casos, há uma tendência natural de querer discutir o que será realizado na próxima Sprint, mas essa é uma matéria da Planning e não da Sprint Review.

> **DICA:** Muitos times praticam o pré-Review, que é um momento ainda sem a participação de todos os stakeholders, onde o Product Owner realiza o QA funcional ao vivo na frente do time. É uma boa prática, pois melhora a capacidade de se apresentar o valor criado pelo time e discute-se novas formas de se realizar a demonstração pública.

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e apresentar o resumo da Sprint|
|Squad|Preparar e apresentar ao vivo as funcionalidades entregues|
|Cliente|Dar seu feedback sobre a Sprint e testar as novas funcionalidades|

#### 5) Retrospectiva

Na Retrospectiva, o Squad deve analisar métricas e opiniões qualitativas para priorizar e decidir alterações internas do time. É uma cerimônia que procura atingir o objetivo da melhoria contínua do time, identificando e retirando potenciais gargalos, e compartilhando aprendizados com as demais equipes.

O primeiro passo é a análise das métricas ágeis que o Squad está mapeando na sua Sprint, incluindo o Velocity, Release Report, Burndown, Cycle Analysis, entre outros.

Com a análise de métricas, o time deve propor, de forma democrática (i.e., há diversos exercícios que se propõem a incentivar a participação de todos) o que não funcionou na Sprint e precisa ser melhorado. Deve haver sempre uma priorização, pois trata-se de uma melhoria de processo de forma incremental, ágil, e não radical.

Também são discutidas se as melhorias propostas nas Retrospectivas anteriores levaram a algum impacto positivo e se o time decide continuar praticando as mesmas nas futuras Sprints.

>**DICA:** Depois de discutidas e agrupadas as propostas pelos times, deve-se decidir por implementar poucos temas estratégicos (e.g., 2 iniciativas mais votadas). Também deve-se mapear inicialmente poucas métricas, pois elas por si só geram informações valiosas. Depois de exauridas as melhorias sobre as métricas mais tradicionais, o time pode buscar métricas mais avançadas, como por exemplo aquelas de [código fonte](https://www.gitprime.com/product/).

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Apresentar feedback sobre os gargalos priorizados na Retrospectiva anterior|
|Scrum Master|Fornecer métricas e apresentar as primeiras análises sobre gargalos da Sprint|
|Squad|Apresentar outros gargalos que não foram identificados pelo Scrum Master|
|Squad|Votar nos prioritários e apresentar sugestões de melhoria para a próxima Sprint|

## Artefatos

Os principais artefatos foram mencionados acima. Resumidamente, os três principais são:

1. **Backlog do Produto:** lista ordenada das Estórias que serão entregues pelo Squad em várias Sprints.
2. **Backlog da Sprint:** lista ordenada das Estórias e as suas Tasks que serão entregues pelo Squad em uma determinada Sprint.
3. **Release Report:** utilizado como medida do valor (Estórias) criado para os usuários do produto.

> [Contribuia](/CONTRIB.md) com os nossos Guides
