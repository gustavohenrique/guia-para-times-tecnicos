# Metodologias Ágeis

Antes de explicar sobre como trabalhamos é necessário um conhecimento prévio sobre metodologias, técnicas e termos existentes que nos inspiram à sempre querer alcançar o máximo da eficácia na criação de produtos digitais.

## O que é Metodologia Ágil?

Metodologia Ágil é um conjunto de métodos que ajudam os times a pensar e trabalhar de forma mais eficaz e tomar melhores decisões. Mais do que isso, Ágil também é um mindset que ajuda as pessoas a compartilhar informações umas com as outras para tomar decisões importantes sobre o projeto juntas, ao invés de ter um gerente que toma as decisões sozinho.
Um mindset Ágil é sobre estar aberto ao planejamento, design e melhorias no processo.

## Story Mapping

Um pré-requisito para construir um produto de sucesso é a eficácia, que é fazer certo a coisa certa, e para isso é necessário o entendimento correto do que precisa ser feito de forma compartilhada com todos os envolvidos. O produto nasce primeiro como uma idéia e logo depois o idealizador possui no máximo algumas noções sobre funcionalidades que ele acha serem necessárias no produto. Mas um produto não é apenas um conjunto de funcionalidades. **Ele precisa entregar valor para quem o utiliza.**

Entender como entregar valor e quais os caminhos necessários para realizar esse trabalho é extremamente difícil de ser feito em uma reunião ou troca de emails. É preciso dinamismo para conseguir extrair essas informações e compartilhar o entendimento delas com o cliente e quem vai colaborar na criação do produto.

 **Story Mapping é uma técnica para criar um entendimento do produto contando estórias a partir do ponto de vista do usuário.** A dinâmica é centrada no usuário e com isso entendemos como vai ser a experiência dele com o software, como o produto o torna uma versão melhor de si, quais os fluxos e qual o mínimo que pode ser feito para entregar valor (MVP).

As estórias são pequenas e simples descrições de uma funcionalidade dita da perspectiva da pessoa que deseja a nova capacidade, usualmente um usuário ou um cliente do sistema - pense sempre que temos vários "client sides" em um produto, como por exemplo usuário final, o administrador, a equipe de operações, etc. Ao criar o mapa delas, conseguimos transmitir o entendimento de forma simples e ágil para todos.

Seguimos como referência a metodologia do livro User Story Mapping: Discover the Whole Story, Build the Right Product. Você pode ler um [resumo](/content/usm.md) dos 7 primeiros capítulos, mas aconselhamos a leitura do texto original. Assista também a um vídeo da LinuxConfAu 2018 onde o método é explicado:

[![](https://cdn1.iconfinder.com/data/icons/material-audio-video/20/play-circle-fill-128.png)](https://www.youtube.com/watch?v=J3VaaPYshek)

## Cascata vs Ágil

![](/content/img/agilevswaterfall.jpg)

O modelo tradicional de Cascata vem sendo utilizado ao longo dos anos por muitas empresas. Embora muitos projetos tenham sido construídos dessa maneira, problemas relacionado à prazos, desperdícios, qualidade e expectativa eram comuns. Em 2001, um grupo de 17 pessoas percebeu que havia um padrão nos problemas de desenvolvimento de software e que a culpa não era dos envolvidos e sim do processo. Esse grupo se reuniu para tentar encontrar uma maneira diferente de pensar sobre esses problemas e assim criaram o [Manifesto Ágil](http://agilemanifesto.org/iso/ptbr/manifesto.html) .
Uma equipe seguindo o processo Cascata tenta escrever o mais cedo possível uma descrição completa do software que precisa ser construído. Uma vez que todos os usuários, gerentes e executivos concordam sobre o que exatamente o software deve fazer, eles entregam um documento descrevendo todos esses requisitos aos desenvolvedores, que devem entregar exatamente o que está escrito. Depois, uma equipe de testes verifica se o software realmente seguiu o que foi escrito no documento.

![](/content/img/waterfall.png)

Esse modelo funciona apenas em um caso: **quando você sabe exatamente tudo que o software deve fazer** . Ná prática, isso raramente vai acontecer.
As principais características do modelo em Cascata são:

- Exige uma descrição completa do software no início do projeto para depois construir exatamente o que foi escrito
- Perde-se muito tempo analisando e discutindo funcionalidades que talvez nunca serão utilizadas
- Não responde bem à mudanças pois o foco está na documentação em vez da colaboração
- Quando se termina o software muitas das regras de negócios mudaram ao longo dos meses e é necessário alterar o software
- O cliente irá visualizar alguma coisa apenas perto do fim do projeto
- Frustração do cliente quando o software faz o que foi pedido mas não da maneira esperada

 **O desenvolvimento de software Ágil é baseado em uma abordagem incremental e iterativa.** Em vez de um planejamento aprofundado no início do projeto, o Ágil está aberto às mudanças de requisitos ao longo do tempo e encoraja feedback constante dos usuários. Os times multifuncionais trabalham em iterações de um produto ao longo de um período de tempo, e este trabalho está organizado em um backlog priorizado com base no valor do negócio ou do cliente. O objetivo de cada iteração é produzir um produto funcionando.

![](/content/img/agile.png)

As principais características que diferem o modelo Ágil do Cascata são:

- Entendimento compartilhado por todos os envolvidos e não uma documentação empurrada
- O planejamento como time é mais importante do que documentar demais um plano e segui-lo
- Diminuição da expectativa dos clientes por entregas frequentes
- Rápida adaptação a mudanças pois o clico de desenvolvimento é dividido em iterações curtas
- Maior visibilidade do que está sendo feito por cada membro do time
- Aprendizado sobre o produto e os usuários antes do final do projeto
- Práticas e ritos para manter o objetivo do projeto alinhado com todos

## Manifesto Ágil

O Manifesto Ágil reconhece que a utilização de processos, ferramentas, documentação, contratos e planos pode ser importante para o sucesso do projeto, mas são ainda mais importantes os chamados valores Ágeis:

- Os indivíduos e suas interações acima de procedimentos e ferramentas;
- O software funcionando acima de documentação abrangente;
- A colaboração com o cliente acima da negociação e contrato;
- Responder à mudanças acima de um plano pré-estabelecido;

Ou seja, mesmo havendo valor nos itens à direita, valorizamos mais os itens à esquerda. Além dos quatro valores instituídos, firmou-se ainda um conjunto de abordagens de desenvolvimento de softwares que pode ser apresentado por meio de 12 princípios:

- Nossa maior prioridade é satisfazer o cliente através da entrega contínua e adiantada de software com valor agregado.
- Aceitar mudanças de requisitos, mesmo no fim do desenvolvimento. Processos ágeis se adequam a mudanças para que o cliente possa tirar vantagens competitivas.
- Entregar frequentemente software funcionando, de poucas semanas a poucos meses, com preferência à menor escala de tempo.
- Pessoas de negócio e desenvolvedores devem trabalhar diariamente em conjunto por todo o projeto.
- Construir projetos em torno de indivíduos motivados. Dando a eles o ambiente e o suporte necessário, e confiando neles para fazer o trabalho.
- O método mais eficiente e eficaz de transmitir informações para e entre uma equipe de desenvolvimento é através de conversa face a face.
- Software funcionando é a medida primária de progresso.
- Os processos ágeis promovem desenvolvimento sustentável. Os patrocinadores, desenvolvedores e usuários devem ser capazes de manter um ritmo constante indefinidamente.
- Contínua atenção a excelência técnica e bom design aumenta a agilidade.
- Simplicidade: a arte de maximizar a quantidade de trabalho não realizado é essencial.
- As melhores arquiteturas, requisitos e designs emergem de times auto-organizáveis.
- Em intervalos regulares, a equipe reflete sobre como se tornar mais eficaz e então refina e ajusta seu comportamento de acordo.

Com o Manifesto Ágil foi necessário uma organização que se configurasse permanente e o representasse. Então, no final de 2001, nasceu a Agile Alliance, uma organização sem fins lucrativos que procura promover o conhecimento e discussões sobre os vários métodos ágeis.

## Mais sobre Metodologias Ágeis

Uma metodologia ágil é uma coleção de práticas combinadas com idéias, conselhos e muitas vezes um conjunto de conhecimentos e riqueza de experiências entre praticantes ágeis. Ela descreve diferentes funções e responsabilidades para todos no projeto.

### Scrum

Scrum é uma metodologia usada para a gestão dinâmica de projetos, que permite controlar de forma eficaz e eficiente o trabalho, potencializando as equipes que trabalham em prol de um objetivo em comum. Ele não é uma metodologia completa, sendo apenas uma estrutura sem fornecer os detalhes encontrados em outras metodologias. **Ele fornece uma definição básica dos papéis, atividades principais e artefatos básicos.**

Não existe uma fórmula padrão que pode ser repetida em todo projeto, pois o Scrum não é baseado em um modelo previsível, mas baseado em um modelo empírico - afirmando que o conhecimento vem da experiência e de tomada de decisões baseadas no que é conhecido - e portanto considera-se que os times vão descobrir a melhor maneira de fazer o trabalho, experimentando coisas, inspecionando quais são os resultados e adaptando seu trabalho para obter melhores resultados no futuro.

O Scrum emprega uma abordagem iterativa e incremental, executadas em ciclos de duas ou quatro semanas denominadas Sprint, para aperfeiçoar a previsibilidade e o controle de riscos.

 **O Times Scrum são auto-organizáveis e multifuncionais, compostos pelo Product Owner, o Time de Desenvolvimento e o Scrum Master.**
Times auto-organizáveis escolhem qual a melhor forma para completarem seu trabalho, em vez de serem dirigidos por outros de fora do time. **Times multifuncionais possuem todas as competências necessárias para completar o trabalho sem depender de outros que não fazem parte da equipe** .

#### Valores

- Transparência: ter uma visão clara e objetiva de todo o processo e uma boa comunicação;
- Inspeção: averiguar com certa frequência os artefatos e progressos do projeto;
- Adaptação: mudar quando for necessário para se ajustar às mudanças e evitar repetir os mesmos erros.

#### Eventos

- Reunião de planejamento da Sprint: o Time Scrum discute e planeja o que pode ser entregue no intervalo da Sprint;
- Reunião diária: O Scrum Master e o Time de Desenvolvimento alinham o que foi feito desde a última reunião diária, o que pretendem fazer nas próximas 24h e se há algum impedimento;
- Reunião de revisão da Sprint: Uma reunião informal entre o Time Scrum e os Stakeholders para demonstrar e inspecionar o que foi feito na Sprint, discutir sobre os problemas que ocorreram na Sprint e adaptar o Product Backlog se necessário;
- Retrospectiva da Sprint: é uma oportunidade para o Time Scrum inspecionar a si próprio e criar um plano para melhorias a serem aplicadas na próxima Sprint.

#### Papéis

- Product Owner (PO): responsável por gerenciar o Backlog do Produto (lista de tarefas ou funcionalidades);
- Time de Desenvolvimento: realizam o trabalho de entregar uma versão usável que potencialmente incrementa o produto "Pronto" ao final de cada Sprint;
- Scrum Master (SM): conduz os eventos do Scrum e remove os impedimentos que o time relatou na Reunião Diária.

#### Artefatos

- Product Backlog: é uma lista ordenada de tudo que deve ser necessário no produto e é uma origem única dos requisitos para qualquer mudança a ser feita no produto;
- Sprint Backlog: é um conjunto de itens do Product Backlog selecionados para a Sprint, juntamente com o plano para entregar o incremento do produto e atingir o objetivo da Sprint.

Times Scrum entregam produtos de forma iterativa e incremental, maximizando as oportunidades de realimentação. Entregas incrementais de produto "Pronto" garantem que uma versão potencialmente funcional do produto esteja sempre disponível.

Obs.: em geral, a brainn.co utiliza o Scrum com Sprint de 2 semanas, pelo menos, em seus contratos.

### eXtreme Programming (XP)

Extreme Programming é um processo para times pequenos e médios e que irão desenvolver software com requisitos vagos e em constante mudança, que busca agregar o máximo de valor possível ao produto com base em feedback e partindo da premissa de que o cliente deve sempre estar lado a lado com desenvolvimento do projeto, aprendendo e gerando feedback o mais cedo possível.

O nome Extreme Programming é proposital para demonstrar radicalidade. Ela funciona trazendo todo o time em conjunto para práticas simples, com feedback suficiente para permitir que todos os membros possam acompanhar o desenvolvimento do projeto e tenham uma visão única.

XP é bem sucedida porque enfatiza a satisfação do cliente. Em vez de entregar tudo o que o cliente quer no futuro, esse processo entrega o software que o cliente precisa, conforme ele precisa. Em um curto espaço de tempo o cliente terá um produto que possa ser utilizado, podendo aprender com o mesmo e reavaliar se o que foi desenvolvido é realmente o desejado.

#### Valores

- Comunicação: para obter sucesso é necessária muita interação entre os membros da equipe, desenvolvedores e cliente;
- Simplicidade: incentiva as práticas que reduzem a complexidade do sistema. A solução adotada deve ser sempre a mais simples para se alcançar os objetivos esperados;
- Feedback: as respostas às decisões tomadas devem ser rápidas e visíveis;
- Coragem: alterar um código em produção, sem causar bugs, com agilidade, requer muita coragem e responsabilidade;
- Respeito: todos têm sua importância dentro da equipe e devem ser valorizados e respeitados, sabendo ouvir e compreender o ponto de vista do outro.

#### Práticas

- Cliente sempre presente: o cliente é um membro da equipe que deve estar lado a lado ao desenvolvimento do projeto, gerando feedback e aprendendo com o sistema, escrevendo critérios de aceitação e definindo prioridades;
- Reunião Diária: tem por objetivo atualizar a equipe sobre o que foi implementado no dia anterior e trocar experiências das dificuldades enfrentadas. Neste momento também são decididas as tarefas que serão implementadas no dia e os responsáveis por elas;
- Jogo do Planejamento: é o momento onde o cliente solicita as funcionalidades desejadas através de estórias, onde a equipe estima o custo de cada estória e planeja as releases e as iterações;
- Programação em Dupla: o código é revisado enquanto está sendo construído, enquanto um desenvolvedor digita, o outro observa, pensa em melhorias e alternativas;
- Desenvolvimento guiado por testes (TDD): o teste automatizado é escrito antes da implementação do código para garantir o funcionamento do que foi feito;
- Refatoração: é um conjunto de técnicas para simplificar e melhorar o código. Todo desenvolvedor, ao encontrar um código duplicado, pouco legível ou lento, tem por obrigação melhorar esse código sem mudar o comportamento dele;
- Código Coletivo: cada desenvolvedor tem acesso a qualquer parte do sistema e tem liberdade para alterá-la a qualquer momento e sem qualquer tipo de aviso;
- Código Padronizado: se os desenvolvedores seguirem um padrão pré-acordado de codificação, mais fácil será manter e entender o que já foi feito;
- Simplicidade de Projeto: o código está na forma mais simples e clara facilitando a compreensão e possível continuidade por qualquer um de seus membros;
- Metáfora: utilização de metáforas para que clientes e desenvolvedores sejam capazes de estabelecer uma vocabulário apropriado para o projeto, repleto de nomes representando elementos físicos com os quais os clientes estejam habituados em seu dia-a-dia, de modo a elevar a compreensão mútua;
- Semana de 40 horas: os desenvolvedores não são produtivos se estiverem cansados e indispostos;
- Integração Continua: depois de testada, cada nova funcionalidade deve ser imediatamente sincronizada entre todos os desenvolvedores para que, caso algum problema seja encontrado, alguém possa corrigir imediatamente;
- Pequenos Lançamentos: implementação de um pequeno conjunto de funcionalidades que ao termino será colocado em produção.

#### Papéis

- Analista de Testes: responsável em garantir a qualidade do sistema através dos testes escritos. Ele deve ajudar o cliente a escrever os Casos de Testes e no final de cada iteração verificar se o software atende todos os casos de testes;
- Gerente de Projetos: é um facilitador no fluxo de comunicação do projeto e serve de ponte entre a equipe, o cliente e eventuais fornecedores. Também é responsável por filtrar assuntos não relevantes aos desenvolvedores e aspectos que só devam ser implementados em iterações futuras;
- Desenvolvedores: trabalham em duplas para analisar, projetar e codificar o software;
- Coach: responsável pelas questões técnicas do projeto, verificando o comportamento da equipe em relação ao processo, sinalizando eventuais erros cometidos.

### Kanban

A palavra Kanban é japonesa e significa cartão sinalizador. Escrita com K maiúsculo se refere ao método e com k minúsculo ao quadro utilizado em metodologias ágeis.
 **O Kanban não é uma metodologia e muito menos um sistema para gerenciamento de projetos.** É um método simples para melhoria de processos e adaptável a quase qualquer tipo de cultura, que busca a evolução, não a revolução. **Trabalha com o sistema de produção puxado, exigindo que cada operação do processo seja alimentada pela demanda da etapa anterior.** A demanda para se trabalhar em uma nova funcionalidade seria gerada quando alguma outra fosse entregue. É utilizado no Sistema Toyota de Produção (TPS) e também por diversas empresas que aderiram à filosofia Lean para representar um sinal para que se puxe mais trabalho e o processo seja alimentado.

 **O quadro kanban é diferente do quadro de tarefas utilizado no Scrum. Em Kanban o que você vê não são tarefas e sim Itens de Trabalho.** Um Item de Trabalho é uma unidade de trabalho independente que pode ser rastreada por todo do processo. No Scrum, por exemplo, o time seleciona as estórias no backlog (Itens de Trabalho) para incluir na Sprint e então quebra elas em tarefas. A medida que as tarefas se movem no quadro de tarefas, os Itens de Trabalho começam a se mover da coluna "To Do" para a coluna "Done". **Logo, uma estória apenas se move entre "To Do", "Doing" e "Done".**

#### Valores

- Comece com o que você já faz hoje: mapeie o seu fluxo de trabalho atual, crie formas de ter visibilidade sobre o que está sendo trabalhado e busque evoluir o processo.
- Busque mudanças incrementais: melhore sempre e sem ser radical. Grandes mudanças ocasionam desafios de comunicação, dificuldades no aspecto técnico e, geralmente, afetam a capacidade produtiva de uma equipe.
- Respeite o processo atual, seus papéis, responsabilidades e cargos: não mude drasticamente a forma como sua organização está estruturada. Faça melhorias evolutivas e não seja disruptivo.

#### Práticas

- Visualize o fluxo de trabalho: divida o trabalho em partes, escreva cada demanda em um cartão e tenha visão de todo o trabalho que está em andamento. Além disso, nomeie colunas para ilustrar onde cada demanda está no fluxo de trabalho.
- Limite o trabalho em progresso: atribua limites explícitos para a quantidade de itens que podem estar em andamento em cada etapa do fluxo de trabalho.
- Meça e gerencie o fluxo de trabalho: tenha visibilidade de quanto tempo as demandas que passam pelo processo têm levado para serem concluídas e remova os impedimentos que por ventura estejam bloqueando o fluxo de trabalho.
- Torne as políticas explícitas: defina, divulgue e socialize o processo, assim todos terão uma clareza de como ele funciona e de como o trabalho realmente é feito. Exemplos de políticas são os critérios para as transições entre as etapas do fluxo de trabalho e o limite de trabalho em progresso.
- Desenvolva loops de feedback: reduza o tempo do ciclo de feedback, pois quanto mais tardia a entrega, mais demorada será a geração de valor daquilo que foi trabalhado.
- Melhore de forma colaborativa: exerça a filosofia de melhoria contínua baseada no kaizen, promovendo pequenas alterações no processo que causem menor resistência à mudança.

#### Eventos

- Reunião diária: Similar à reunião do Scrum;
- Reuniões de planejamento de releases: servem para definir quando novos incrementos do projeto serão instalados em produção.

## Monitoramento e Métricas

### Burndown Chart

Consiste em um gráfico utilizado para representar diariamente o progresso do trabalho em desenvolvimento. Ou seja, após cada dia de trabalho o gráfico apresenta a porção de trabalho finalizada em comparação com o trabalho total planejado.

![](/content/img/burndown.png)

### Diagrama de Fluxo Cumulativo

O Cumulative Flow Diagram (CFD) é um gráfico atualizado diariamente que demonstra a distribuição do trabalho entre as fases do processo, ou seja, como um Item de Trabalho está se movendo através do sistema. Ao olhar para ele, você verá instantaneamente como está o desempenho da equipe. Se tudo funcionar perfeitamente, as faixas estarão equilibradas. Nada de sobressaltos ou aumentos repentinos, apenas a faixa Tarefas Completas devem subir.

![](/content/img/cfd.png)

### Velocidade

O gráfico de velocidade demonstra o quanto um time está conseguindo entregar de valor ao longo do tempo. A sua medida pode ser em número de tarefas realizadas ou story points ao longo de um determinado período. Oscilações podem indicar um problema de produtividade da equipe, endógeno (fatores que foram gerados pelo próprio time, como por exemplo um membro da equipe que tenha ficado doente) ou exógeno (fatores que são alheios ao time, como por exemplo uma atividade precedente que o cliente não cumpriu no prazo combinado). O importante é que o time utilize o gráfico de velocidade para ter uma conversa produtiva sobre o que melhorar nas sprints seguintes para que a velocidade seja mantida num nível saudável.

![](/content/img/velocity.png)

## Nossa Metodologia

Na brainn.co utilizamos User Story Mapping na fase que chamamos de Product Discovery, que acontece após a assinatura do contrato com o cliente. Após essa fase criamos um entendimento bem claro sobre o produto. Com esse entendimento, conseguimos dimensionar o tamanho do time, criar um plano de lançamento de versões (roadmap) e definir como vamos aprender com o software para construir o que realmente vai entregar valor.

Não nos prendemos à apenas uma metodologia ágil. Utilizamos práticas do Scrum, XP e Kanban. Não há uma metodologia específica porque isso varia de acordo com o projeto e o cliente. Além dos princípios no Manifesto Ágil, também adotamos nossos próprios princípios no dia-a-dia:

- Compartilhe o que você conhece, aprenda e cresça junto com o time;
- Crie um ambiente orientado à missão e não à tarefas;
- Trabalhe sem ego, ninguém no time é melhor do que o outro;
- Tire as idéias da cabeça e compartilhe com o time;
- Valide as hipóteses ao invés de perder tempo discutindo sobre achismos;
- Não basta apenas fazer certo. É preciso fazer certo a coisa certa;
- Faça a coisa certa primeiro, então faça bem feito;
- Fazer bem feito a coisa certa não é suficiente, é preciso entender o motivo;
- Para o Ágil funcionar, é necessário mais do que pessoas inteligentes;
- Pessoas não são apenas recursos substituíveis, elas causam impactos;
- Seja inteligente quando houver obstáculos no caminho;
- Mantenha o time alinhado com os objetivos para entregarem valor;
- Deixe as pessoas livres para fazerem o trabalho delas;
- Entenda os prós e os contras de dizer às pessoas o que devem fazer;
- As práticas utilizadas devem fazer a diferença;
- Experimente e assuma os riscos;
- Membros do time de desenvolvimento devem ser multidisciplinares;
- Os papéis do Scrum não são necessariamente cargos na empresa;
- Pare de procurar culpados e de focar nas consequências das falhas;
- Aprenda com os erros e evite que o mesmo aconteça novamente.

> [Contribuia](/CONTRIB.md) com os nossos Guides
