# Módulo 1 - Aula 1 - Tipos de Dados e Variáveis
Na primeira aula, tivemos um breve primeiro contato com a linguagem _Python_, explorando superficialmente alguns detalhes
sobre ela.

Mas se você saiu com a sensação de que não aprendeu nada, fique tranquilo:<br>
O conteúdo aqui descrito deve lhe dar uma visão mais clara sobre o conteúdo abordado.

## Literais
Vamos revisitar um programa exibido na última aula rapidamente, agora alterado para o português:

```python
# Arquivo: intro.py
print("Olá, mundo!")
```

Se você bem se recorda, esse programa apenas imprime (ou _exibe_, de certa forma, para simplificar) o texto `Olá, mundo!` na saída do
console, parecendo, desse modo, pouco útil para nós.

Veja a saída do programa:



> [!NOTE]
> Não se preocupe agora com jargões específicos da área da programação; eles serão explicados ao longo das aulas.
> Por agora, entenda o _console_ como uma janela de um aplicativo em que podemos digitar comandos.

Mas nas entrelinhas desse código tão simples, teremos nosso primeiro aprendizado efetivo:<br>
Compreenderemos o que são os _literais_.

---

### Literais por toda a parte
Olhe mais atentamente para o código do programa; você verá uma linha acinzentada e uma outra linha com diferentes colorizações.
A linha acinzentada, iniciada em `#`, demarca um _comentário_, ou seja, um trecho do arquivo de código-fonte que será ignorado pelo
interpretador Python - o software que nos permite executar ('rodar') os programas que desenvolvemos.

Por serem ignorados, os comentários são usados para explicar ou tornar mais claro um trecho de código, mas falaremos disso em outro
momento.

Por agora, foque nessa linha em específico:

```python
print("Olá, mundo!")
```

Mesmo sem ainda termos elucidado algumas questões - tais como _'O que exatamente é `print`?_ - podemos notar que _print_, do inglês
'imprimir' é o que faz a frase ser exibida na tela (mesmo que _como_ ele o faz ainda pareça um mistério).<br>
Mas, se tudo em programação é composto de código, magia negra e termos ininteligíveis, o que é `"Olá, mundo!"`?

Essa pequena frase entre aspas duplas é um **_literal_**.<br>
Em programação, um **_literal_** é qualquer valor 'puro' diretamente escrito no código-fonte.

No nosso simples programa, temos apenas um literal: `"Olá, mundo!"` - um valor diretamente escrito no código-fonte.<br>
Apenas isso: valores diretamente escritos no código-fonte.

Ou seja, se tivermos um arquivo Python assim:

```python
# Arquivo: exemplo_literais.py
print("Bom dia")
print(5)
print(27.4)
print("a")
```

O que teremos é uma série de `print`s que imprimem literais: todos os valores entre parênteses no código acima são literais.

_Mas eles não são diferentes?_, você pode ter se perguntado...<br>
Sim, eles são. Mas para explorar essa diferença, teremos primeiro que explorar um penúltimo tópico:

As _variáveis_.

## Variáveis
Até agora, só vimos literais em ação.<br>
Para entender o que são variáveis, analise o código abaixo comigo (que, propositalmente, contém um erro).<br>
Não se preocupe em entender o que é `input` agora, apenas siga o fluxo comigo:

```python
# Arquivo: bom_dia_usuario.py
input("Qual o seu nome? ")
print("Bom dia, nome!!")
```

Nesse código-fonte, embora vocês ainda não tenham aprendido, temos uma função `input` que, ao ser executada, vai exibir o literal<br>
`"Qual o seu nome? "` no console e aguardar por uma entrada de caracteres, aceita quando o usuário apertar a tecla _Enter_.

Quando o usuário pressionar _Enter_, a função aceitará a entrada de caracteres dele, para que então possamos imprimir seu nome no
`print`.

_Exceto_ pelo fato de que o programa **_não_** imprime o nome do usuário.

---

### Nomes e denominações
Tente executar o programa acima, caso esteja curioso.<br>
Você se deparará com a seguinte saída no console:

```
>>> Qual o seu nome? <Carlos>
>>> Bom dia, nome!!
```

> [!NOTE]
> Aqui estarei usando como convenção:<br>
> * O símbolo `>>>` para indicar uma saída de caracteres do console.
> * Os símbolos `<` e `>` ao redor de texto insierido no console por alguém.

Perfeito, não?<br>
_Porquê isso acontece?_, você deve estar se perguntando...

Por duas razões, mas vamos à primeira:<br>
`"Bom dia, nome!!"` é um literal, ou seja, um valor diretamente inserido no código-fonte - `nome` não representa o nome do usuário,
é apenas uma parte do literal que inserimos no código.

Já a segunda requer mais conhecimento para ser notada...
Onde o _Carlos_ foi parar?<br>
Ele foi aceito pela função `input`, então, onde ele está?

---

### Onde entram as expressões
Expressões e _statements_ são tópicos que quero abordar futuramente, mas cujo entendimento superficial auxiliará a compreensão
de variáveis.

* Expressões são trechos de código que _retornam um valor_.
  Em Python, por exemplo, `5 + 3` retorna o valor `8`.
* Um _statement_ é uma linha de código que performa uma ação ou um (ou mais) 'comandos' (tais como execução de funções) 


### Alterando com literais, literalmente
Sabemos teoricamente o que é um literal, então, que tal abranger mais esse conceito e explorar suas implicações na prática?<br>
Abra o arquivo `ola_mundo.py` que temos usado até aqui e tente substituir o literal `"Olá, mundo!"` por outro literal qualquer.

Sim, exatamente isso que passou pela sua mente: _como assim?_<br>
Acalme-se, jovem.

Apenas delete o literal e coloque outro no lugar.<br>
Uma frase, um número, o que desejar: apenas digite o que quiser, e veja as mudanças provocadas por essa alteração quando executar o
programa.

> [!TIP]
> Caso você não se recorde:<br>
> Para executar um programa através de IDEs populares, basta localizar o botão _Executar_ ou _Run_.<br>
> Para executar um programa através da linha de comando, basta digitar `python3 <nome_do_arquivo>` e apertar _Enter_.

A depender do que você inseriu, o literal terá sido exibido, _impresso_ na tela.<br>
Ou você será agraciado com uma mensagem de erro.

Em caso de erro, apenas deixe-o de lado por enquanto, e mantenha-se atento.

---

### Um literal no meu console
Vamos supor, por exemplo, que no lugar do nosso literal `"Olá, mundo!"` você tenha inserido o número 5.<br>
Muito provavelmente, o número 5 terá sido exibido em sua tela.

Mas, o que ele é, exatamente?<br>
Você já sabe a resposta: um **_literal_**.

Porém, como você inseriu o número 5?<br>
* `5`
* `"5"` ou `'5'`
* `"\u0035"`

_Não se assuste, apenas ignore a última._

O que acontece é que (_rufem os tambores_) `5` ou `"5"` são, ambos, literais.<br>
Mas são literais de _diferentes tipos_.

## Tipos de Dados
O que ocorre é que, em computação, lidamos o tempo todo com dados: abrimos uma planilha `.xlsx` no Excel com vários
números, editamos um documento `.docx` no Word repleto de palavras, ouvimos um áudio `.mp3` de uma música no celular...

Em todos esses exemplos, e na verdade, sempre que estamos _usando_ qualquer dispositivo que contenha uma placa eletrônica
com algum chip, estamos lidando com dados.

E esses dados possuem diferentes tipos, afinal, faria sentido, por exemplo, tratar uma batata-doce como um ovo?<br>
Ou um pedaço de ferro como um bolo?

São analogias esdrúxulas, mas que servem para mostrar que, assim como nós lidamos com os objetos e itens do dia a dia de
acordo com seus _tipos_, sistemas eletrônicos e programáveis o fazem pelos seus _tipos de dados_.

Desse modo, vamos entender e explorar essas definições.

---

### Dados específicos, sem especificação
Como havia dito, um literal `5` e outro literal `"5"` são ambos, literais, mas de diferentes tipos de dados.

Embora, para os iniciantes, isso não esteja aparente.

Por exemplo, digitar:

```python
print(5)
```

Ou:

```python
print("5")
```

Não parece provocar diferenças.<br>
Sob execução, os dois códigos produzem o mesmo resultado final: o número 5 que conhecemos é impresso na tela.

Mas repare: o tom de cor usado para realçar os dois literais são _levemente desiguais_.

A justificativa para tal é essa:<br>
* `5` é um literal de número inteiro, ou seja, seu _tipo_, em Python, é `int`, recebendo uma cor levemente mais escura
* `"5"` é um literal de _string_, ou seja, seu _tipo_, em Python, é `str`, recebendo uma cor levemente mais clara


> [!TIP]
> <details>
>  <summary>O que é uma <em>string</em>?</summary>
>
>  _String_ é um termo da área para designar uma sequência de caracteres.
>
>  Considerando que _string_, em inglês, denomina algo como 'cordão' ou 'barbante', pode-se visualizar um literal de
>  _string_ qualquer como um conjunto de caracteres _ligado_ entre si por 'cordões' ou 'barbantes'.
>
>  Por exemplo:<br>
>  O literal `"Bom dia"` pode ser visto como `B_o_m_ _d_i_a`, em que cada `_` pode ser entendido como um 'cordão',<br>
>  ligando os caracteres entre si.
>
>  E _sim_, o espaço entre as duas palavras _é_ um caractere.<br>
>  Mas deixemos isso para depois.
> </details>

Mas, se a diferença é, aparentemente, significativa, porquê há tão baixa indicação visual disso?

---

### A especificação que faltava
O que ocorre é que Python é uma linguagem de _tipagem dinâmica_.<br>
Isso significa que os literais 
