# Introdução

O valor da informação vai além das palavras escritas, números e imagens: conhecimento, conceitos, idéias e marcas são exemplos de formas intangíveis da informação. Em um mundo interconectado, a informação e os processos relacionados, sistemas, redes e pessoas envolvidas nas suas operações, são informações que, como outros ativos importantes, têm valor para o negócio da organização e, consequentemente, requer proteção contra vários riscos.  
A segurança da informação é a proteção de informações contra ameaças. Todas as pessoas na organização que têm contato com algum tipo de informação precisam receber um treinamento sobre segurança da informação.  
Algumas razões para implementar um sistema de gerenciamento de segurança da informação:

- Garantir a continuidade do negócio
- Minimizar riscos
- Maximar o retorno do investimento
- Diferencial competitivo de mercado
- Governança corporativa
- Atendimento aos requisitos de segurança dos clientes
- Em alguns casos poder ser usada como vantagem no marketing

Esse documento contém normas e propostas para implementar um sistema de gerenciamento de segurança da informação (SGSI) com o objetivo de *chegar o mais próximo possível sem perder agilidade* do cumprimento da norma ISO/IEC 27001, que define os requisitos para que os mecanismos de controle consigam garantir a **confidencialidade**, **integridade** e **disponibilidade** da informação.  

# Normas

## 1. Escopo

As normas descritas nesse documento são para a prática de gestão de segurança da informação levando em consideração os riscos existentes e possíveis ameaças que possam afetar a brainn ou seus clientes.  
Fazem parte do escopo dessas normas:

- Ficar o mais próximo possível da conformidade com a norma ISO/IEC 27001 sem perder agilidade;
- Implementar controles de segurança da informação que sejam aceitos pelos sócios e partners;
- Desenvolver nossos próprios princípios de gestão da segurança da informação.

## 2. Referências normativas

A inspiração para esse documento veio das normas ISO/IEC 27001 e ISO/IEC 27002. A família ISO/IEC 27000 é composta por dezenas de normas relacionadas a segurança da informação, certificada e com confiança comprovada, servindo como base para outros modelos de governança como ITIL e COBIT.  
A ISO/IEC 27001 estabelece *requisitos mandatórios* para planejar, implementar, monitorar e analisar o SGSI e é usada como base para auditoria de certificação da empresa. Já a ISO/IEC 27002 traz *recomendações* de controles para o anexo A da 27001 e não pode ser usada como base para auditoria.

## 3. Termos e definições

- **Informação:** conjunto de dados que tem significado em algum contexto.
- **Confidencialidade:** Propriedade da informação relacionada a exclusividade e privacidade, que não é disponibilizada à quem não tem acesso.
- **Integridade:** Propriedade da exatidão e completeza da informação.
- **Disponibilidade:** Propriedade da informação ser acessível e utilizada sob demanda para quem precisa e tem autorização.
- **Incidente:** Evento indesejado de causa desconhecida.
- **Ameaça:** Algo que ainda não ocorreu mas pode ocorrer para causar um incidente.
- **Problema:** Quando um incidente tem uma causa conhecida.
- **Vulnerabilidade:** Uma fraqueza que pode ser explorada por uma ameaça.
- **Risco:** Probabilidade de uma ameaça explorar uma vulnerabilidade e causar danos.

## 4. Estrutura desta Norma

### 4.1 Seções

Cada seção que define os controles de segurança da informação contém um ou mais objetivos de controle. Esse documento aborda as seções da ISO/IEC 27002 que se referem ao anexo A da ISO/IEC 27001:

- [Seção A.5 Política de segurança da informação PSI](#5-política-de-segurança-da-informação-psi)
- [Seção A.6 Organização da segurança da informação](#6-organização-da-segurança-da-informação)
- [Seção A.7 Segurança em recursos humanos](#7-segurança-em-recursos-humanos)
- [Seção A.8 Gestão de ativos](#8-gestão-de-ativos)
- [Seção A.9 Controle de acesso](#9-controle-de-acesso)
- [Seção A.10 Criptografia](#10-criptografia)
- [Seção A.11 Segurança física e do ambiente](#11-segurança-física-e-do-ambiente)
- [Seção A.12 Segurança nas operações](#12-segurança-nas-operações)
- [Seção A.13 Segurança nas comunicações](#13-segurança-nas-comunicações)
- [Seção A.14 Aquisição, desenvolvimento e manutenção de sistemas](#14-aquisição-desenvolvimento-e-manutenção-de-sistemas)
- [Seção A.15 Relacionamento na cadeia de suprimentos](#15-relacionamento-na-cadeia-de-suprimentos)
- [Seção A.16 Gestão de incidentes em segurança da informação](#16-gestão-de-incidentes-em-segurança-da-informação)
- [Seção A.17 Aspectos da segurança da informação na gestão da continuidade do negócio](#17-aspectos-da-segurança-da-informação-na-gestão-da-continuidade-do-negócio)
- [Seção A.18 Conformidade](#18-conformidade)

### 4.2 Categorias de Controle

Cada seção principal contém:

- um **objetivo** de controle declarando o que se espera ser alcançado;
- um ou mais **controles** que podem ser aplicados para se alcançar o objetivo de controle.

## 5. Política de segurança da informação (PSI)

> **Objetivo:** Prover uma orientação e apoio da direção para a segurança da informação, de acordo com os requisitos do negócio e com as leis e regulamentações relevantes.

A Política de segurança da informação (PSI) é o documento que registra os princípios e as diretrizes adotadas pela organização e que devem ser seguidos por todos. É recomendado haver uma revisão do documento a cada 3 meses pelo responsável dela ou após os resultados das avaliações de gerenciamento, que mostram se determinada medida está sendo seguida ou não e se faz sentido mante-la ou não. Depois de escrita, deve ser comunicada para a organização inteira.  
Esse documento pode ser encontrado no [Repositório de Documentos](psi.md) e deve permanecer acessível para todos os integrantes da empresa.

## 6. Organização da segurança da informação

> **Objetivo:** Estabelecer uma estrutura de gerenciamento, para iniciar e controlar a implementação da segurança da informação dentro da organização e garantir a segurança das informações no trabalho remoto e no uso de dispositivos móveis.

### 6.1 Organização interna

Todas as responsabilidades pela segurança da informação devem ser definidas e atribuídas.

| Papel | Descrição | Responsável |
|-------|-----------|-------------|
| **Chief Information Security Officer (CISO)** | O chefe da segurança da informação desenvolve a estratégia de segurança geral para todo o negócio. | Gustavo Henrique |
| **Information Securty Manager (ISM)** | O gerente da segurança da informação ajuda a desenvolver a política de segurança e garente que ela seja observada | Todos os sócios e partners |
| **Chief Executive Office (CEO)** | O diretor executivo fica responsável pela segurança das informações do negócio | Thiago Aragão |

#### Versionamento de código fonte de softwares

- Cada cliente deve ter seu próprio grupo no Gitlab onde ficarão seus repositórios;
- Se o cliente exigir que seja utilizado um repositório que não seja administrado pela brainn, então o líder técnico deve sincronizar o código junto à um repositório da empresa antes da reunião de planejamento de cada sprint;
- Todo repositório deve conter um ícone que representa ou identifica o cliente e uma descrição em português ou inglês;
- O líder técnico e o PO de cada time devem ser responsáveis por gerenciar as permissões dos usuários e criar os repositórios dentro do grupo;
- Por padrão, membros do time de um cliente não devem ter acesso aos repositórios de outros clientes. Caso seja necessário o acesso, deve haver uma solicitação via email informando o motivo para o CISO, para o líder técnico e PO do outro projeto.

#### Armazenamento de documentos digitais

- Documentos e arquivos que precisam ser compartilhados com pessoas de fora da organização devem ser armazenados no Google Drive;
- Documentos confidenciais como contratos, propostas, planejamento estratégico, informações financeiras e dados pessoais dos funcionários, devem ser armazenados no repositório Git para registrar quando e quem alterou o conteúdo;
- O CEO gerencia quem tem permissão para acessar os documentos de negócio da empresa;

#### Conscientização sobre segurança da informação

- O CISO fica responsável pela divulgação de conteúdo e a política de segurança para conscientizar as pessoas;
- Cada ISM deve ajudar a solucionar as dúvidas sobre segurança que os funcionários possam ter.

#### Melhoria do SGSI

- Cada ISM deve verificar se alguma norma de segurança está impactando negativamente um processo e relatar ao CISO;
- O CISO deve rever o SGSI frequentemente com base nos feedbacks obtidos de cada ISM.

### 6.2 Dispositivos móveis e trabalho remoto

#### 6.2.1 Política para o uso de dispositivo móvel

- O proprietário de um smartphone deve sempre ficar próximo e nunca se afastar dele;
- Dispositivos contendo dados privados ou confidenciais não devem se conectar à redes sem fio inseguras;
- O sistema operacional e os sotwares instalados devem estar sempre atualizados;
- Todos os dispositivos devem utilizar senhas de bloqueio automático;
- Não é permitida a alteração da configuração dos sistemas operacionais pelos usuários dos equipamentos de propriedade da organização;
- No caso de furto ou roubo de um dispositivo móvel fornecido pela organização, o usuário deve notificar imediatamente o ISM ou o CISO e procurar a ajuda das autoridades policiais registrando um boletim de ocorrência (BO);
- Dispositivos utilizados para o desenvolvimento de software devem utilizar unidades e mídias criptografadas para armazenamento de dados e instalação de softwares;
- Não deve ser instalado o sistema operacional Windows em nenhum dispositivo fornecido pela empresa sem uma passar por uma análise de risco do CISO.

#### 6.2.2 Trabalho remoto

- Não deve ser permitido o acesso de familiares e visitantes ao equipamento utilizado para o trabalho;
- O ambiente não deve apresentar risco de roubo ou furto ao equipamento;
- O dispositivo só pode ser conectado à uma rede segura e protegida por um firewall;
- O profissional deve ficar disponível online no período acordado com o time do qual faz parte.

## 7. Segurança em recursos humanos

> **Objetivo:** Assegurar que funcionários e partes externas entendam suas responsabilidades e estejam em conformidade com os papéis para os quais eles foram selecionados, que estão conscientes e cumprem as suas responsabilidades pela segurança da informação e proteger os interesses da organização como parte do processo de mudança ou encerramento da contratação.

### 7.1 Antes da contratação

A organização deve assegurar que funcionários e partes externas entendam suas responsabilidades e estejam em conformidade com os papéis para os quais eles foram selecionados, enviandos primeiramente os documentos *política de segurança da informação* e *política de desenvolvimento de software*.

#### 7.1.1 Seleção

A organização deve confirmar:

- As informações pessoais e o endereço de residência fornecidos pelo futuro funcionário;
- Informações acadêmicas e profissionais;
- Condições físicas e mentais para exercer o trabalho, especialmente se a for algo crítico para a organização.

#### 7.1.2 Termos e condições de contratação

- Todos os funcionários, fornecedores e partes externas que tenham acesso a informações sensíveis devem assinar um termo de confidencialidade ou de não divulgação (NDA);
- Os funcionários devem ser informados sobre as responsabilidades legais com relação às leis de direitos autorais e legislação de proteção de dados;
- Os funcionários devem estar cientes e de acordo sobre suas responsabilidades com o tratamento da informação recebida de outras empresas ou partes interessadas, como não divulgar para terceiros por exemplo;
- Devem ser informadas as ações a serem tomadas no caso de o funcionário ou partes externas, desrespeitar os requisitos de
segurança da informação da organização;
- Os papéis e responsabilidades pela segurança da informação devem ser comunicados para o candidato durante o processo de pré-contratação;
- O funcionário deve receber o código de conduta da empresa.

### 7.2 Durante a contratação

A organização deve assegurar que os funcionários e partes externas estão conscientes e cumprem as suas responsabilidades pela segurança da informação.

#### 7.2.1 Responsabilidades da direção

Convém que as responsabilidades da direção assegurem que os funcionários e partes externas:

- Estão de acordo com os termos da seção [7.1.2](#7-1-2-termos-e-condições-de-contratação) antes de obterem acesso às informações sensíveis ou sistemas;
- Saibam que devem reportar violações nas políticas e procedimentos de segurança da informação para o ISM e CISO.

#### 7.2.2 Conscientização, educação e treinamento em segurança da informação

- Todos na organização devem ser notificados via email quando houverem atualizações regulares da política de segurança da informação;
- A organização deve fornecer um programa de conscientização da segurança da informação que pode ser através de artigos, videos, livros ou workshops;
- A organização deve utilizar o canal `#security` no slack para notificação sobre falhas de segurança descobertas.

#### 7.2.3 Processo disciplinar

A organização deve comunicar que pode tomar ações contra funcionários que tenham cometido uma violação de segurança da informação, cuja punição, dependendo da gravidade e do impacto causado, pode ser desde de uma advertência formal até a quebra de contrato de prestação de serviços.

### 7.3 Encerramento e mudança da contratação

Para proteger os interesses da organização como parte do processo de mudança ou encerramento da contratação, é necessário:

- Deixar claro ao funcionário que qualquer NDA assinado ainda é válido e precisa ser respeitado;
- Desativar quaisquer acessos à softwares, serviços e conteúdo particular da empresa e de cada projeto;
- Certificar de que todos os equipamentos, dispositivos e materiais de propriedade da empresa que foram fornecidos para a realização do trabalho sejam devolvidos em perfeitas condições;
- Recolher chaves, cartões de acesso, crachá e qualquer outro item que possibilite o acesso físico dentro da empresa;
- Avisar aos outros funcionários, fornecedores e terceiros envolvidos para não mais compartilhar esta informação com a pessoa que está saindo.

## 8. Gestão de ativos

> **Objetivo:** Identificar os ativos da organização e definir as responsabilidades apropriadas para a proteção dos ativos e assegurar que a informação receba um nível adequado de proteção, de acordo com a sua importância para a organização.

### 8.1 Responsabilidade pelos ativos

- Deve haver um registro de todos os ativos em uma base de dados. As informações mínimas são o *tipo*, *proprietário*, *localização*, *classificação* e *valor para o negócio*;
- Todo software comprado (ou grupo de softwares) deve possuir um proprietário cuja responsabilidade é definir quem pode utilizar e ser o "administrador" dele;
- Todos os funcionários e partes externas devem devolver os ativos que estejam em sua posse, após o encerramento de suas atividades, do contrato ou acordo;
- Funcionários ou partes externas cuja as atividades executadas são importantes, devem documentar e transferir todas as informações para a empresa.

### 8.2 Classificação de ativos de informação

Todo ativo de informação deve:

- Receber um nível adequado de proteção, de acordo com a sua importância para a empresa e valor de negócio (*alto*, *médio* e *baixo*);
- Ser classificado como *confidencial*, *restrito*, *uso interno* e *público*;

Exemplo:

|Ativo|Tipo|Proprietário|Localização|Classificação|Valor|
|-----|----|------------|-----------|-------------|-----|
|Gitlab|saas|CISO|http://gitlab.com|Uso interno|Alto|
|Notebook Acer|notebook|CEO|escritório|restrito|Médio|
|Product Discovery|metodologia|CEO| -|público|Alto|

## 9. Controle de acesso

> **Objetivo:** Limitar o acesso à informação e aos recursos de processamento da informação, assegurar acesso de usuário autorizado e prevenir acesso não autorizado a sistemas e serviços.

- Pedidos de acesso devem ser socilitados via email para o proprietário do ativo;
- Os direitos de acesso de usuários devem ser revisados em intervalos regulares e depois de quaisquer mudanças, como promoção, remanejamento ou encerramento do contrato;
- Os direitos de acesso da pessoa devem ser removidos ou suspensos em caso de férias ou afastamento das atividades;
- Todos os acessos permitidos a cada ativo devem ser registrados em uma base de dados;
- Os usuários devem ser orientados a seguir as práticas da PSI para criação de senhas;
- Os softwares para gestão de informação da empresa (contabilidade, home banking, planilhas, contratos...) devem ser acessados através de um dispositivo único com acesso restrito e localizado fisicamente dentro da empresa.
- Deve ser utilizado um sistema de gerenciamento de senhas que possibilite a criação de senhas fortes, que permita criar um grupo de usuários para gerenciar a permissão ao grupo e que consiga registrar quando e quem solicitou determinada senha;
- A [política de desenvolvimento de software (PDS)](pds.md) deve ser analisada para a criação de produtos digitais.

## 10. Criptografia

> **Objetivo:** Assegurar o uso efetivo e adequado da criptografia para proteger a confidencialidade, autenticidade e/ou a integridade da informação.

- As chaves geradas para um sistema não devem ser reutilizadas por outros;
- As chaves devem ser distribuídas para os usuários devidos;
- As chaves devem ser revogadas quando forem comprometidas ou o usuário deixar a empresa;
- Deve haver um backup das chaves de segurança.

## 11. Segurança física e do ambiente

> **Objetivo:** Prevenir o acesso físico não autorizado, danos e interferências com os recursos de processamento das informações e as informações da organização.

- Visitantes não devem ficar sozinhos no escritório;
- Assuntos sigilosos devem ser discutidos apenas em espaços com isolamento acústico;
- Documentos confidenciais em papel devem ser guardados em gaveteiros com fechadura e apenas pessoas autorizadas podem ter uma cópia das chaves;
- Equipamentos devem ser protegidos contra falta de energia elétrica e outras interrupções causadas por falhas elétricas;
- Apenas os sócios têm permissão para permitir a remoção de ativos para fora do escritório;
- Deve ser adotada uma política de mesa limpa na qual as informações do negócio sensíveis ou críticas, por exemplo, em papel ou em mídia de armazenamento eletrônicas, sejam guardadas em lugar seguro;
- Deve ser adotada uma política de tela limpa bloqueando ou desligando as estações de trabalho ao se afastar do computador.

## 12. Segurança nas operações

> **Objetivo:** Garantir a operação segura e correta dos recursos de processamento da informação.

- A utilização do repositório Git deve ser documentada para usuários que não são desenvolvedores;
- Os usuários do Git devem ser conscientizados à não versionar senhas, chaves criptográficas ou informações confidenciais;
- Mudanças na organização, nos processos do negócio, nos recursos de processamento da informação e nos sistemas que afetam a segurança da informação, devem ser controladas através de um processo de gerenciamento de mudanças, capaz de verificar se os requisitos de segurança foram atendidos, qual o impacto da mudança para o negócio, etc;

## 13. Segurança nas comunicações

> **Objetivo:** Garantir a proteção das informações em redes e dos recursos de processamento da informação que os apoiam.

Nenhuma das diretrizes se aplicam à brainn nesse momento devido a empresa não possuir uma infra estrutura de rede própria e utilizar conexões gerenciadas pelo fornecedor de coworking.

## 14. Aquisição, desenvolvimento e manutenção de sistemas

> **Objetivo:** Garantir que a segurança da informação é parte integrante de todo o ciclo de vida dos sistemas de informação. Isto também inclui os requisitos para sistemas de informação que fornecem serviços sobre as redes públicas.

- Os requisitos relacionados com segurança da informação devem ser incluídos nos requisitos para novos sistemas de informação ou melhorias dos sistemas de informação existentes;
- Deve ser avaliado o nível de proteção requerida para manter a confidencialidade e integridade das informações. Se a informação possuir um alto valor para o negócio, o sistema deve possuir um elevado nível de controle de acesso e permitir efetuar cópias de segurança;
- O desenvolvimento de sistemas deve seguir a [política de desenvolvimento de software (PDS)](pds.md) da organização.

## 15. Relacionamento na cadeia de suprimentos

> **Objetivo:** Garantir a proteção dos ativos da organização que são acessíveis pelos fornecedores.

Nenhuma das diretrizes se aplicam à brainn nesse momento.

## 16. Gestão de incidentes em segurança da informação

> **Objetivo:** Assegurar um enfoque consistente e efetivo para gerenciar os incidentes de segurança da informação, incluindo a comunicação sobre fragilidades e eventos de segurança da informação.

- Funcionários e fornecedores devem ser avisados a não tentar provar suspeitas de fraquezas de segurança;
- Um processo mais aprofundado sobre gerenciamento de incidentes pode ser aplicado em um momento futuro da empresa.

## 17. Aspectos da segurança da informação na gestão da continuidade do negócio

> **Objetivo:** É recomendado que a continuidade da segurança da informação seja considerada nos sistemas de gestão da continuidade do negócio da organização.

Nenhuma das diretrizes se aplicam à brainn nesse momento.

## 18. Conformidade

> **Objetivo:** Garantir que a segurança da informação está implementada e operada de acordo com as políticas e procedimentos da organização.

- Uma análise crítica independente deve ser iniciada pela direção;
- A análise crítica deve ser executada por pessoas independentes da área avaliada;
- Se forem usados teste de invasão ou avaliações de vulnerabilidades, devem ser tomadas precauções uma vez que tais atividades podem conduzir a um comprometimento da segurança do sistema.

# Outros documentos

- [Política de Segurança da Informação - PSI](psi.md)
- [Política de Desenvolvimento de Software - PDS](pds.md)

> Saiba como [contribuir](/CONTRIB.md)
