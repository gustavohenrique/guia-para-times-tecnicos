# Boas práticas para escrever código

Não basta escrever um código bom. Ele precisa ser mantido sempre limpo.
Os princípos descritos aqui foram inspirados nos livros "Clean Code" e "Code Complete 2". Recomendamos fortemente a leitura desses clássicos do mundo do desenvolvimento de software.

## Nomes significativos

### Use nomes que revelem seu propósito.

Exemplo de variável que guarda um determinado dia:

    d = 30 # Bad
    dia_pagamento = 30 # Good

### Evite informações erradas.

No caso abaixo, lista de compras não é um nome bom pois parece que a variável é do tipo `list` quando na verdade é apenas um `dict` :

    lista_de_compras = {'item': 'arroz', 'item': 'feijao'} # Bad
    lista_de_compras = ['arroz', 'feijao'] # Good

### Faça distinções significativas

Jamais utilize números para distinguir métodos e variáveis:

    # Bad
    user1 = User()
    user2 = User()

    # Good
    manager = User()
    employee = User()

### Use nomes pronunciáveis e sem abreviações

Se não for fácil de falar, vai ser difícil de entender:

    dt_pagt # Bad
    data_pagamento # Good

### Evite mapeamento mental

Variáveis de uma letra como i, j, k, c são tradicionalmente utilizadas dentro de loops e por isso são traduzidas mentalmente como variáveis auxiliares. Melhor do que utiliza-las é descrever o que elas significam:

    for i in [2015, 2016, 2017]: # Bad
    for year in [2015, 2016, 2017]: # Good

### Nomes de classes

Classes e objetos devem ter nomes com substantivo, como Cliente, TelaCadastro, Endereco.

    class Pagar # Bad
    class Pagamento # Good

### Nomes de métodos

Os nomes de métodos devem ter verbos como salvar, excluir, deletar.

    def salva(): # Bad
    def salvar(): # Good

### Padronize nomes de métodos

Não use palavras diferentes para o mesmo conceito. Se na classe `Usuario` foi criado o método `salvar` para persistir a informação no banco de dados então não faz sentido o método que persiste as informações do pedido se chamar `criar` .

    cliente.salvar()
    pedido.criar() # Bad

    cliente.salvar()
    pedido.salvar() # Good

### Use nomes utilizados pelos usuários do software

Se existe um processo de cadastro de usuário que no domínio de negócio do cliente é chamado de optin, então manter esse nome pode ser uma boa escolha.

## Métodos e Funções

### Identação

Idente sempre o código utilizando espaços ou tabs de acordo com as boas práticas da linguagem utilizada. Configure o editor ou IDE para utilizar espaços ou tabs automaticamente.

### Encoding

Utilize sempre UTF-8. Versões antigas do Windows utilizam por padrão ISO-8859-1 então configure o editor ou IDE para salvar automaticamente no formato UTF-8.

### Faça apenas uma coisa

Os métodos devem ter apenas uma responsabilidade. Devem fazer apenas uma coisa, e faze-la bem.

    # Bad
    def get_user_authenticated(user_id):
     user = User.get(id=user_id)
     user.last_access = datetime.now()

O exemplo acima é uma má prática pois o método está fazendo duas coisas: 1. obter um usuário de acordo com o ID e 2. definir a data do ultimo acesso. O melhor seria:

### Evite o uso do switch sempre que possível

Switchs tendem à crescer e com isso a manutenção fica prejudicada. Felizmente Python não suporta switch/case. Uma alternativa é usar dicionários:

    titles = {
     1: "Página Inicial",
     2: "Serviços",
     3: "Contato"
    }
    page_id = 3
    title = titles.get(page_id, "Página não encontrada")
    print(title) # Contato

### Use nomes descritivos

Os nomes dos métodos devem descrever exatamente o que fazem. Não tenha medo de escrever nomes longos. Um nome longo e descritivo é melhor do que um nome curto e enigmático.

    // Javascript
    exibirTabela() # Bad
    exibirTabelaContendoEnderecosCadastrados(); # Good

### Parâmetros de métodos

A quantidade ideal de parâmetros é zero. Até dois é aceitável mas acima disso é extremamente desaconselhável.
Se necessário enviar muitas informações para um método, passe através de objetos, lists ou dicts.

    # Bad
    def writeXml(name, dir, content)

    # Good
    xml = {
     'name': 'payments.xml',
     'dir': '/tmp/',
     'content': '<payment><date>2017-06-01</date><value>1234.50</value>'
    }
    def write(xml)

### Verbos e palavras chaves

O nome do método e seu argumento devem formar um belo par verbo/substantivo. O ideal é que a chamada ao método explique a intenção do que é esperado.

    subscription.cancel_subscription(1234) # Bad
    subscription.cancel_by(id=1234) # Good

### Tratamento de Erros

Métodos devem fazer apenas uma coisa. Tratamento de erro é uma coisa. Crie um método para tratamento de erro.

### Evite duplicidade de código

Dont’t Repeat Yourself ou DRY, é um princípio para evitar a duplicidade de código extraindo o que for repetido para um novo método.

    // Java
    void salvar(Usuario usuario) {
     if (usuario != null && usuario.nome != "" && usuario.senha != "") {
     ... // rotina para salvar usuario
     }
    }

    void atualizar(Usuario usuario) {
     if (usuario != null && usuario.nome != "" && usuario.senha != "") {
     ... // rotina para atualizar usuario
     }
    }

No código acima a condição está repetida nos dois métodos. Quando a condição é extraída para um novo método chamado isValid o código fica melhor:

    // Java
    boolean isValid(Usuario usuario) {
     return usuario != null && usuario.nome != "" && usuario.senha != "";
    }

    void salvar(Usuario usuario) {
     if (isValid(usuario)) {
     ... // rotina para salvar usuario
     }
    }

    void atualizar(Usuario usuario) {
     if (isValid(usuario)) {
     ... // rotina para atualizar usuario
     }
    }

### Não use null

Métodos retornando null ou None são uma péssima idéia mas passar null como parâmetro é pior ainda. Evite enviar/receber null. Utilize um objeto vazio, uma string em branco ou zero para números. Mas não null.

## Comentários

### Maus comentários

Não comente um código ruim. Reescreva-o.
Um dos maiores motivos para escrita de comentários é o código ruim. Comentários escritos para tentar explicar um código confuso e desorganizado devem ser evitados. Refatore o código e deixe-o mais expressivo. Qual código é mais fácil de entender? Assim:

    # Verifica se o funcionario está apto a receber todos os benefícios.
    if funcionario.motivoDemissao != 1 and funcionario.idade > 65:

Ou assim?

    if funcionario.pode_receber_todos_beneficios():

### Bons comentários

Algumas vezes comentários são necessários ou benéficos. Por exemplo, se você está escrevendo uma API ou uma lib que vão ser utilizados por outros, os comentários podem complementar a documentação. Docstrings nesses casos são bem-vindos, mas não exagere.

### Comentários Legais

Algumas vezes somos forçados a escrever comentários por razões legais. Em projetos de código aberto (Open Source) por exemplo, dependendo da licença escolhida, é necessário inserir em cada arquivo de código fonte um resumo da licença no topo do arquivo.

### Comentários byAuthor

Comentários que informam o nome do autor só fazem sentido se você é o único que pode alterar o código. Se trabalha em time então outro programador pode alterar seu código. Se o código foi escrito para uma empresa ou cliente, então não é só seu. Se deseja rastreabilidade, saber quem criou ou alterou, então os logs do controlador de versão (svn/git) podem fornecer essas informações.

### Comentários óbvios

Dãããããã…

    """ Retorna o nome """
    def get_nome()

Não faça nada do tipo.

## Convenções de Código para cada Linguagem

Convenções de código melhoram a legibilidade do código e permitem que outros programadores possam entender o código mais rapidamente.
utilize, se houver, as boas práticas da linguagem de programação escolhida. Em Python a mais utilizada é a PEP8.
Existem ferramentas que verificam se o código está de acordo com essas regras. São ferramentas de análise estática ou linters.
Acostume a utilizar no seu editor/IDE ou a rodar antes de fazer o `commit` do código.

> Saiba como [contribuir](/CONTRIB.md)
