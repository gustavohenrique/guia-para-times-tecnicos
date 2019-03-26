# Metodologia de Projetos

## Introdução

Na empresa, utilizamos métodos e princípios ágeis para geração do máximo valor para os stakeholders dos nossos projetos. Praticamos nossa própria metodologia baseada no Scrum, Kanban e XP em projetos de escopo flexível, permitindo que os valores do [Manifesto Ágil](http://agilemanifesto.org/) sejam respeitados no dia-a-dia, por meio de papéis, artefatos e cerimônias praticados pelos nossos Squads.

## Responsabilidades

### Product Owner

O PO é a ligação entre o time e o cliente. Sua responsabilidade é entender e discutir sobre o produto com o cliente, tirar dúvidas e tomar decisões em relação ao produto. Ele deve evitar qualquer tentativa de contato do cliente com o time.

### Scrum Master

O SM é responsável por conduzir as cerimônias e ajudar o time à remover impedimentos que estejam impactando no projeto. Além disso, ele também pode fornecer informações para o PO sobre o andamento do projeto ou métricas.

### Time de Desenvolvimento

É o time composto pelos engenheiros responsáveis pela implementação do produto. A responsabilidade desse time é definir e estimar suas próprias tarefas, se comprometer a executar o que eles mesmos definiram como Backlog da Sprint, participar das cerimônias e comunicar rapidamente qualquer bloqueio que possa atrasar a entrega do trabalho.

### Time de Apoio ao Produto

Consiste em pessoas que produzem o trabalho necessário para que o time de desenvolvimento e os stackeholders tenham insulmos para seguir em frente no desenvolvimento do produto. Esse time pode ser composto por várias pessoas porém cada papel é realizado por apenas uma pessoa (e.g., Designer, Copywriter, Growth Hacker...).

Esse time tem participação opcional nas cerimônias que envolvem o Time de Desenvolvimento. O Time de Apoio ao Produto deve ter suas próprias cerimônias com o PO, seja como um time ou individualmente.

## Cerimônias

As cerimônias são eventos necessários para dar visibilidade à todos os envolvidos sobre o andamento do projeto, possibilidades de melhorias, dificuldades, realizações e melhorar a comunicação do time.

### 1) Grooming (Refinamento do Backlog)

Um passo opcional, sempre antes da Planning, quando o time precisa ter um entendimento melhor de uma Estória para poder quebra-la em uma Estória menor.  É uma atividade de background que demanda algum tempo recorrente (e.g., 1 hora por semana), mas que traz um valor enorme aos Squads do projeto. Exemplos de benefícios:

- Auxilia na priorização das Estórias pelo Product Owner se comparado com o Valor de Negócio
- Permite o time a tomar decisões mais bem informadas em relação a futuras Estórias da Release
- Explicita deficiências de entendimento em relação ao Backlog do Produto antes de uma Planning
- Indica ao Product Owner quando uma Estória está muito complexa e precisa ser quebrada

As Estórias têm pesos associados pelo time por meio de Pontos das Estórias, que é uma medida relativa de esforço e risco, ou seja, pode-se usar uma medida arbitrária contato que exista consistência do peso utilizado para as Estórias ao longo das Sprints (e.g., uma Estória de 2 pontos de uma Sprint deve representar o dobro de dificuldade em relação a uma Estória de 1 ponto de qualquer Sprint, passada ou atual).

Deve-se sair do exercício com os Critérios de Aceitação (também chamados de Condições de Satisfação) das Estórias, justamente porque os mesmos dão fundamento às estimativas de Pontos das Estórias dadas pelo time.

>**DICA:** Alguns [erros](https://medium.com/bynder-tech/12-common-mistakes-made-when-using-story-points-f0bb9212d2f7) devem ser evitados:
- Não usar as referências históricas para o peso relativo de Estórias
- Não quebrar Estórias em Estórias menores, mais granulares e fáceis de observar no Burndown
- [Associar pontos com Tasks](https://www.mountaingoatsoftware.com/blog/dont-estimate-the-sprint-backlog-using-task-points),  quando a verdadeira intenção é mapear gargalos nos fluxos das Tasks
- Não aprofundar o entendimento de uma Estória quando diferentes membros do time dão estimativas muito díspares
- Modificar os Pontos das Estórias ao longo da Sprint ao invés de discutir isso com o time na Retrospectiva

Nada impede que o Product Owner valide posteriormente eventuais dúvidas que surgiram no Grooming e que requerem uma pesquisa mais aprofundada, o que poderá por sua vez alterar a estimativa dos Pontos da Estória no próximo Grooming ou na Planning.

Na realidade, a função do Product Owner é diariamente melhorar o seu [entendimento sobre a UX](https://uxchecklist.github.io/), decidindo com os stakeholders o que o produto deve conseguir fazer primeiro, executando dinâmicas de User Story Mapping constantemente ao longo das Sprints.

> **DICA:** A pior coisa que pode acontecer a um Product Owner é ficar estrito a documentação de Estórias. Sua curiosidade e poder de convencimento deve também levar os stakeholders a se convencerem que as suas sugestões fazem sentido. A comprovação pode ser simplesmente subjetiva como baseada em dados primários ou secundários. Se houver Tasks que o time tenha que executar para refutar uma determinada hipótese, essa deve entrar no Backlog do Produto.

Indicamos de forma resumida os papéis e responsabilidades dos membros do time:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e o Backlog do Produto seja atualizado|
|Product Owner|Antes do Grooming, documentar os objetivos, valor de negócio, usuários envolvidos, sketches, benchmark, e os critérios de aceitação das Estórias da Release atual|
|Time|Estimar o esforço para a entrega das Estórias utilizando como referência outras Estórias já entregues, indicando quando uma Estória precisar ser quebrada|
|Time|Indicar se houver risco técnico ou de segurança relacionado a uma Estória, indicando alternativas ou validações por meio de POC|

### 2) Sprint Planning

É uma reunião na qual se planeja o trabalho a ser realizado na Sprint. O Time e o Product Owner negociam, a partir das Estórias do Product Backlog do Produto **priorizadas**, o que será desenvolvido. Facilitados pelo ScrumMaster, eles selecionam um conjunto de Estórias do Backlog do Produto que julgam ser capazes de desenvolver na duração da Sprint, o que é apenas uma previsão, e estabelecem um objetivo ou meta de negócios a ser alcançada com o desenvolvimento dessas Estórias, chamada de Meta da Sprint.

>**DICA**: No decorrer do desenvolvimento do produto, é normal acontecer uma diminuição da demanda de trabalho para o Time de Apoio ao Produto e a Sprint Planning desse time ser bem rápida. Nesse caso, vale testar uma alteração no período da Sprint, talvez diminuir para 1 semana ou aumentar para 3 semanas.

Passos para realizar uma Sprint Planning eficaz:

#### a) Criar Definições

Há 3 definições importantes antes de começar cada Sprint:

1. **Definição da Meta da Sprint:** objetivo da Sprint, qual o valor que vai ser entregue. Ex.: Permitir que o usuário faça o cadastro, login e visualiza os produtos à venda no ecommerce.  
2. **Definição de Preparado (Definition of Ready - DoR):** o que é necessário para uma Estória entrar na Sprint. Ex.: Priorização e entendimento sobre o que precisa ser feito.
3. **Definição de Pronto (Definition of Done - DoD):** o que é necessário para uma Estória ser considerada como concluída ao final da Sprint. Ex.: Deploy realizado em Staging para testes de QA.

#### b) Definir o Backlog da Sprint

Na Sprint Planning o Product Owner apresenta o Backlog do Produto priorizado, explicando ao time quais são os objetivos de curto prazo do projeto e o que eles deveriam entregar primeiro para gerar valor ao cliente o mais rápido possível. Em cima dessas explicações, o Time de Desenvolvimento detalha as Estórias mais prioritárias que estarão especificadas a nível de negócio, em nível técnico, de modo que eles consigam gerar estimativas de esforço e dar visibilidade sobre o desenvolvimento.  
O time fecha o escopo quando as estimativas preencherem todo o tempo que terão de desenvolvimento na Sprint e apresenta ao Product Owner. Não havendo objeções, o desenvolvimento começa. O Scrum Master é o responsável por garantir e geralmente conduzir esta cerimônia, fazendo com que as responsabilidades sejam respeitadas.

Ao longo da Sprint, novas Estórias ou Tasks poderão ser adicionadas ao Backlog da Sprint se houver consentimento do time, o que é chamado de Scope Change. Isso deverá ser tratado na Daily.

Quando todas as Tasks forem criadas, a Estória passa para o status Ready.

> **DICA:** Para uma Estória ser considerada Ready e o Time de fato ter o entendimento compartilhado, é recomendado que seja discutido:
- Critérios de Aceitação
- Roteiros de Testes
- Definition of Done
- Sequência de Tasks
- Mudanças nos [User Flows](https://www.smashingmagazine.com/2012/01/stop-designing-pages-start-designing-flows/)
- Revisão da [Arquitetura da Informação](http://alistapart.com/article/thedisciplineofcontentstrategy)
- Ativação de [Métricas](https://uxdesign.cc/ux-tools-for-analytics-and-metrics-51634c3c26ec)
- Validação de Hipóteses (e.g., [Diamante Duplo](https://brasil.uxdesign.cc/ux-design-toolbox-ced4b7f209d0))
- Necessidade de documentação para usuários

Ao longo da Sprint, todos os stakeholders devem ter visibilidade completa sobre o Backlog da Sprint, ajudando a todos identificarem oportunidades de melhorias e gargalos. O uso de ferramentas deve responder ao processo decidido pelo time e não o inverso. A extração de métricas deve ser o mais automatizada possível para não gerar trabalho adicional para o Scrum Master e ser voltada para o objetivo de melhoria contínua e não para a simples cobrança por produção.

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e o Backlog da Sprint seja atualizado|
|Product Owner|Antes da Planning, decidir quais Estórias do Backlog do Produto serão priorizadas para o desenvolvimento|
|Time de Desenvolvimento|De forma sequencial, confirmar os Pontos das Estórias que foram puxadas para a próxima Sprint|
|Time de Desenvolvimento|Contribuir com o cumprimento do checklist para a Estória estar Ready para desenvolvimento|
|Time de Desenvolvimento|Decidir quantas Estórias serão incorporadas no Backlog da Sprint|

### 3) Daily

No decorrer da Sprint, para que o alinhamento não se perca, o Scrum Master deve garantir que diariamente o time se reúna para conversar brevemente, por até 15 minutos, sobre o que cada um está fazendo para alcançar a Meta da Sprint e se tem algo impedindo o avanço. Os impedimentos levantados nesta cerimônia devem ser a prioridade do Scrum Master, enquanto que um desvio do objetivo pode ser consertado fácil e rapidamente pelo Product Owner.

A Daily visa a comunicação síncrona do time, por isso recomenda-se que não se torne um exercício mecânico de simples status update, pois essa é uma prática não ágil. E também deve-se evitar bots de Daily, pois esses incentivam o exercício mecânico e torna um exercício focado na documentação, e perde-se o foco de criar uma verdadeira colaboração e interesse mútuo entre o trabalho dos membros do Time.

A pauta clássica para o que cada um deve informar para os demais:

- O que foi feito desde a última Daily
- O que pretende fazer até a próxima Daily
- Qual ajuda precisará para realizar a sua entrega

Ao término da Daily, o Scrum Master sai com uma lista de to-do para ajudar o time a se tornar mais produtivo, retirando os impeditivos.

Na prática, o Time deve ter uma visão compartilhada do quadro kanban e cada um (ou o Scrum Master) deve mover os cards entre as colunas do quadro de acordo com a alteração no status. O quadro deve ser o guia para cada um conversar sobre o que fez, está fazendo ou pretende fazer.

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
|Time|Comunicar com o time sobre o andamento das Tasks e desafios encontrados|
|Product Owner|Indicar eventuais bugs críticos que tenham surgido no QA|
|Time|Alterar o escopo do Backlog da Sprint, em casos extremos ("Scope Change")|

### 4) Review

Ao término do período da sprint, no último dia, acontece a Sprint Review. A Review é uma cerimônia de inspeção e prestação de contas, onde o time apresenta os avanços desta sprint ao Product Owner e demais stakeholders do projeto. Nessa apresentação o time irá receber feedback para corrigir qualquer desvio do objetivo do produto e gerar melhorias no projeto não previstas inicialmente na Sprint Planning.

Na Review, o Time de Desenvolvimento irá demonstrar o que foi criado ao longo das últimas semanas para todos os stakeholders. A demonstração deve levar cerca de meia hora a uma hora por semana de Sprint.

Independente de ser a primeira ou a última Sprint de uma determinada Release, sempre há o que ser demonstrado, pois os loops de feedback devem sempre ocorrer em um time ágil.

Cada Estória apresentada deve cumprir os Critérios de Aceitação e deve ter passado com sucesso nos Testes.

As Estórias não finalizadas devem ser apresentadas e os feedbacks obtidos dos stakeholders devem ser incorporados pelo Time. Em muitos casos, há uma tendência natural de querer discutir o que será realizado na próxima Sprint, mas essa é uma matéria da Planning e não da Sprint Review.

> **DICA:** Muitos times praticam o pré-Review, que é um momento ainda sem a participação de todos os stakeholders, onde o Product Owner realiza o QA funcional ao vivo na frente do time. É uma boa prática, pois melhora a capacidade de se apresentar o valor criado pelo Time e discute-se novas formas de se realizar a demonstração pública.

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Facilitar que o exercício seja realizado e apresentar o resumo da Sprint|
|Time de Desenvolvimento|Preparar e apresentar ao vivo as funcionalidades entregues|
|Cliente|Dar seu feedback sobre a Sprint e testar as novas funcionalidades|

### 5) Sprint Retrospective

Após a Review, é hora da Sprint Retrospective, a cerimônia de adaptação promovendo a melhoria contínua. O Time irá compartilhar o aprendizado e discutir pontos bons e ruins que aconteceram na última sprint em relação às pessoas, práticas, ferramentas e tudo mais que possa ser melhorado. 

O primeiro passo é cada membro do Time de Desenvolvimento escrever em particular, dentro de um timebox de 10 minutos, o que foi bom e o que pode melhorar e entregar ao Scrum Master. O SM então deve separar o que foi em escrito e permitir que todos tenham visibilidade. Então o Scrum Master lê em voz alta o que foi escrito e pede para quem escreveu explicar o motivo para o restante. No final, os pontos ruins são enumerados e o Time discute possíveis e prioriza soluções para evitar que os problemas aconteçam novamente.

Também são discutidas se as melhorias propostas nas Retrospectivas anteriores levaram a algum impacto positivo e se o time decide continuar praticando as mesmas nas futuras Sprints.

>**DICA:** Depois de discutidas e agrupadas as propostas pelos times, deve-se decidir por implementar poucos temas estratégicos (e.g., 2 iniciativas mais votadas). Também deve-se mapear inicialmente poucas métricas, pois elas por si só geram informações valiosas. Depois de exauridas as melhorias sobre as métricas mais tradicionais, o time pode buscar métricas mais avançadas, como por exemplo aquelas de [código fonte](https://www.gitprime.com/product/).

Indicamos de forma resumida os papéis e responsabilidades dos membros do Squad:

|Papel|Responsabilidades|
|:--------|:--------|
|Scrum Master|Apresentar feedback sobre os gargalos priorizados na Retrospectiva anterior|
|Scrum Master|Fornecer métricas e apresentar as primeiras análises sobre gargalos da Sprint|
|Time|Apresentar outros gargalos que não foram identificados pelo Scrum Master|
|Time|Votar nas soluções prioritárias e apresentar sugestões de melhoria para a próxima Sprint|

## Artefatos

Os principais artefatos foram mencionados acima. Resumidamente, os três principais são:

1. **Backlog do Produto:** lista ordenada das Estórias que serão entregues pelo Time em várias Sprints.
2. **Backlog da Sprint:** lista ordenada das Estórias e as suas Tasks que serão entregues pelo Time em uma determinada Sprint.
3. **Incremento:** resultado do que foi produzido pelo Time durante a Sprint.
4. **Definição de Pronto (Definition of Done - DoD):** documento contendo uma definição comum e clara do que significa quando uma Estória está em "Done". Para o desenvolvedor pode significar que o código está funcionando na máquina dele, para o PO pode significar que está pronto para ser testado por um QA e para o cliente que está funcionando em produção. Por isso é importante definir e alinhar qual vai ser o significado.
5. **Plano da Release:** documento contendo uma data estimada para a Release e quais Estórias do Backlog do Produto são necessárias parte para atingir a Meta da Release.

> [Contribua](/CONTRIB.md) com os nossos Guides
