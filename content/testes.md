# Testes de Software

Todo tipo de teste em software deve ser automatizado para evitar um problema conhecido como "olhar viciado" e para manter a qualidade do código existente.
Olhar viciado ocorre quando quem está testando possui visão parcial de certos problemas e por isso algumas mudanças passam despercebidas.

Tipos de testes que idealizamos na brainn.co:

## Teste Unitário

Um teste unitário é a menor porção que se pode testar em software. É testado uma parte do código no qual dado uma entrada deve retornar uma saída esperada:

- O teste não deve depender de nenhum agente externo (APIs, Filas, Banco de Dados...);
- Testes devem ser independentes e o resultado de um não deve impactar o resultado do outro;
- Deve ser rápido na execução, no máximo alguns segundos cada um.

Exemplo usando Python:

```python

class Calculadora(object):
    def somar(self, num1, num2):
        return num1 + num2

import unittest
class CalculadoraTest(unittest.TestCase):
    def test_soma_de_dois_numeros(self):
        result = Calculadora().somar(2, 2)
        self.assertEqual(4, result)
```

## Teste de Integração

Verifica o funcionamento da integração entre componentes do software. Por exemplo, testar a integração com banco de dados ou sistemas de filas.
É comum em alguns frameworks MVC, Django por exemplo, é comum encontrar testes que utilizam Models para salvar informações no banco de dados. Embora sejam tratados como testes unitários, na verdade são testes de integração.

## Teste de Aceitação

Mais conhecido como teste de QA (Quality Assurance). É o teste que verifica se o que foi desenvolvido atende à todos os critérios de aceitação definidos pelo cliente.
Em projetos que envolvem interface gráfica, esse tipo de teste pode ser automatizado e também ser chamado de Teste de Interface.

## Teste de Interface/Componentes

É um tipo de teste que verifica se as interações entre o usuário e os componentes possuem o comportamento esperado. Por exemplo, testar se um texto digitado no campo email não contém o arroba então deve ser exibido na tela uma mensagem de erro.
A ferramenta mais utilizada para esse tipo de teste em interfaces web é o Selenium Webdriver. Ele possui drivers para diversas linguagens de programação. Entretanto o Webdriver em si requer muitas linhas de código para escrever alguns testes e por isso existem outras libs que atuam como uma camada sobre ele para reduzir a complexidade. Uma delas é o Splinter para Python.

Exemplo:

```python
from splinter import Browser

browser = Browser()
browser.visit('http://google.com')
browser.fill('q', 'brainn.co')
browser.find_by_name('btnG').click()

if browser.is_text_present('hello@brainn.co'):
    print "A busca no google exibe nosso email."
else:
    print "Google nao achou nada da brainn.co"

browser.quit()
```

No exemplo acima, o teste vai abrir uma janela do browser e pesquisar no Google por `brainn.co` e verificar se o resultado da busca retorna o email `hello@brainn.co` .

## Teste A/B

Tem como objetivo validar uma hipótese. É basicamente a comparação de resultados entre duas saídas. Funciona separando de forma transparente alguns usuários para uma experiência alternativa a fim de validar um novo fluxo ou uma nova interface.
Por exemplo, 60% dos usuários seguem para o fluxo A e os outros 40% para B. Com base nas métricas inseridas em B, o cliente pode analisar os resultados e decidir se a experiência B vai se tornar a principal ou vai deixar de existir.

## Teste de Usabilidade

Serve para testar se a interface do usuário é fácil de usar e de entender. Está mais relacionado com processos de design e não pode ser automatizado. Existem softwares que gravam videos mostrando como o usuário interage com a interface. Esse video é analisado depois por profissionais de design para identificar pontos de melhoria.

## Teste de Acessibilidade

Verifica se a interface está de acordo com os padrões exigidos para ser utilizada por deficientes visuais e auditivos.

## Teste de Performance/Stress/Escalabilidade

Esse tipo de teste serve para determinar como um sistema funciona em termos de tempo de resposta, estabilidade e consumo de recursos de hardware e rede.
Há algumas discussões sobre o objetivo do teste de performance, stress e escalabiliadde, porém geralmente os nomes são utilizados para descrever a mesma coisa.

Exemplo para descobrir qual o tempo de resposta de uma API:

```shell
siege --concurrent=50 --content-type="application/json" 'http://example.com/api POST {"key1":"value1","key2":"value2"}'
```

Site do projeto siege: https://www.joedog.org/siege-home/

## Teste de Segurança

Teste de segurança é essencial para previnir acesso de intrusos à softwares que manipulam dados confidenciais. Empresas grandes contratam alguém responsável por executar um pentest (penetration test) definindo o que pode ou não ser feito nesses testes.
Existem ferramentas que varrrem o código escrito pelos desenvolvedores procurando por má práticas no código e outras que automatizam uma parte do trabalho do pentest procurando vulnerabilidades conhecidas.

Leia mais: [Automatizando Testes de Vulnerabilidades em Aplicações Web com o OWASP ZAP e Python](https://medium.com/@gustavoh/automatizando-testes-de-vulnerabilidade-em-aplica%C3%A7%C3%B5es-web-com-o-owasp-zap-e-python-fdcdcf78b587)

> Contribua com os nossos [Guias](/content/github.md)
