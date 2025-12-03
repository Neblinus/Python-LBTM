# Módulo 1 - Aula 1 - Tipos de Dados, Literais e Variáveis
Na primeira aula, tivemos um breve primeiro contato com a linguagem _Python_, explorando superficialmente alguns detalhes
sobre ela.

Mas se você saiu com a sensação de que não aprendeu nada, fique tranquilo:<br>
O conteúdo aqui descrito deve lhe dar uma visão mais clara sobre o conteúdo abordado.

## Tipos de Dados
Vamos revisitar um programa exibido na última aula rapidamente, agora alterado para o português:

```python
# Arquivo: intro.py
print("Olá, mundo!")
```

Se você bem se recorda, esse programa apenas imprime (ou _exibe_, de certa forma, para simplificar) o texto `Olá, mundo!` na saída do
console, parecendo, desse modo, pouco útil para nós.

Veja a saída do programa:

<img src="https://github.com/Neblinus/Python-LBTM/blob/f7810d7300cf9480459d1b262ac0ad8d26a94120/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/HelloWorld.png" alt="Console exibindo a saída 'Olá, mundo!' de um programa Python">

> [!NOTE]
> Não se preocupe agora com jargões específicos da área da programação; eles serão explicados ao longo das aulas.
> Por agora, entenda o _console_ como uma janela de um aplicativo em que podemos digitar comandos.

Mas nas entrelinhas desse código tão simples, teremos nosso primeiro aprendizado efetivo:<br>
Compreenderemos o que são os _tipos de dados_.

## Tipos de Dados
O que ocorre é que, em computação, lidamos o tempo todo com dados: abrimos uma planilha `.xlsx` no Excel com vários
números, editamos um documento `.docx` no Word repleto de palavras, ouvimos um áudio `.mp3` de uma música no celular...

Em todos esses exemplos, e na verdade, sempre que estamos _usando_ qualquer dispositivo que contenha uma placa eletrônica
com algum chip, estamos lidando com dados.

E esses dados possuem diferentes tipos, afinal, faria sentido, por exemplo, tratar uma batata-doce como um ovo?<br>
Ou um pedaço de ferro como um bolo?

São analogias esdrúxulas, mas que servem para mostrar que, assim como nós lidamos com os objetos e itens do dia a dia de
acordo com suas _categorias_, sistemas eletrônicos e programáveis o fazem pelos seus _tipos de dados_.

Desse modo, vamos entender e explorar essas definições.

---

### Dados específicos, com especificação
Python, assim como qualquer linguagem de programação, lida com seja lá quais forem os dados com que estamos trabalhando através
de seus tipos. Mas o que seria um _tipo_?

Vamos retomar o programa do início da aula, focando nessa linha:

```python
print("Olá, mundo!")
```

Nessa linha de código, temos a frase `"Olá, mundo!"`, e ela, surpreendentemente, representa um tipo de dado.
Em termos técnicos, na linguagem Python, uma sequência de caracteres - letras, números, etc - entre aspas simples
`''` ou duplas `""` é considerado uma **_string_**.

> [!TIP]
> <details>
>  <summary>Me explique melhor</summary>
>
>  <strong><em>string</em></strong> é um termo da área para designar uma sequência de caracteres.
>
>  Considerando que _string_, em inglês, denomina algo como 'cordão' ou 'barbante', pode-se visualizar uma
>  _string_ qualquer como um conjunto de caracteres _ligado_ entre si por 'cordões' ou 'barbantes'.
>
>  Por exemplo:<br>
>  `"Bom dia"` pode ser visto como `B_o_m_ _d_i_a`, em que cada `_` pode ser entendido como um 'cordão',<br>
>  ligando os caracteres entre si.
>
>  E _sim_, o espaço entre as duas palavras _é_ um caractere.<br>
>  Mas deixemos isso para depois.
> </details>

Essa categorização define como a linguagem irá interagir com os dados que fornecemos - assim como, por exemplo, nós lidamos com
um rato de laboratório de forma diferente da qual usamos em relação a uma bactéria patogênica.

Vamos a alguns exemplos.

---

### Testando tipos de dados
Para testar o impacto dos tipos de dados no funcionamento da linguagem, vamos tentar fazer algumas operações.<br>
Não se preocupe com os detalhes desconhecidos por agora; eles serão explicados nas próximas aulas.

Em Python, podemos realizar operações diversas e que seriam comuns para nós.

Por exemplo, poderíamos juntar duas _*strings*_, ou seja, duas sequências de caracteres, assim como juntamos frases
ou sílabas para formar textos e palavras, usando o operador de soma (`+`):

```python
# Arquivo: frases.py
print("Eu sou uma frase")
print("Eu sou uma frase" + " e eu sou outra!")
```

Ao executar esse programa, teremos:

<img src="https://github.com/Neblinus/Python-LBTM/blob/c1897b8d22556e49a30e9c80cf72fe198c852bab/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/Frases.png" alt="Programa mostrando duas frases sendo concatenadas em Python">

Como podemos ver, na segunda saída do comando `print`, as strings foram unidas - mais à frente, veremos que o termo certo
seria 'concatenadas'.

Interpretando essa saída sobre a ótica dos tipos de dados, podemos dizer que o interpretador Python - o software que executa
nosso código - usou o operador de soma (`+`) para realizar uma 'soma' de acordo com a definição do que seria 'somar' para
strings.<br>
Sendo elas sequências de caracteres, faz sentido juntá-las.

Vejamos algo semelhante, agora, com números:

```python
# Arquivo: numeros.py
print(5 + 5)
print(5 + 5 - 2)
```

Naturalmente, a saída desse programa é:

<img src="https://github.com/Neblinus/Python-LBTM/blob/1f6704cff122936067ddd0bae03c7602a4c8a78c/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/Numeros.png" alt="Programa demonstrando soma e subtração em Python">

Aqui, o interpretador Python também utilizou a definição de soma - representada no operador `+` - e também de subtração
(operador `-`) para nos trazer o resultado das operações; dessa vez, porém, em se tratando de números.

A partir desses exemplos, podemos ir ao ponto central da definição de tipos de dados.

---

### Onde os dados se desencontram

Embora, para os iniciantes, isso nem sempre esteja aparente, as strings e os números que vimos acima têm significados
completamente díspares - isso porque são de diferentes tipos de dados.

Observe os comportamentos exibidos a seguir.

Se tivermos o seguinte programa, o que ocorrerá durante sua execução?

```python
# Arquivo: tristeza.py
print("A vida castiga cada dia mais" - " e o salário só diminui.")
```

<img src="https://github.com/Neblinus/Python-LBTM/blob/1f3540b9589fcfbec98affcebbe3d1261e926846/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/Tristeza.png" alt="Programa que tenta usar o operador de subtração entre strings.">

Podemos perceber que o interpretador encontrou um erro, explícito na linha `TypeError` - ou seja, um erro referente ao
_tipo_ dos dados utilizados. 

O que causou o erro? Bem...

Para nossa decepção, o nível de infelicidade exibido nessas strings não altera o comportamento do interpretador Python.<br>
O que ocorre é que o operador de subtração (`-`), que havíamos utilizado com sucesso há apenas alguns momentos, no teste com
números, não pode ser utilizado em strings, porquê esse _tipo de dado_ não o suporta.

Para definir isso, analisemos como a linguagem determina esses tipos.

---

### 'Não faz o meu tipo' - ou onde o filho chora e a mãe não vê
Talvez sua cabeça comece a girar agora, por isso, vou dar algumas definições técnicas da forma mais rápida
o possível, para então explicá-las em termos simples. Descanse tranquilo sabendo que logo você entenderá o
significado completo dessas definições (mas não hoje, ainda).

Em Python, tanto as strings que vimos como os números são _objetos_, ou seja, um identificador (ID) associado a um endereço
de memória RAM no _heap_ contendo um valor atribuído a si, sendo instâncias de uma classe padrão da linguagem ou definida pelo
usuário.

~~Uau. Sim. Até o português pode ser ininteligível.~~

Vamos lá.<br>
Em termos de bioquímica e biologia, temos um material genético que armazena informações usadas para todos os processos do
nosso organismo (DNA). Dentre essas informações, acessamos genes específicos para, por exemplo, construir proteínas através
da síntese proteica, em que um códon será correspondente a um determinado aminoácido.

Paramos aqui.<br>
Tanto os números quanto as strings que vimos são como aminoácidos, que correspondem a um códon - uma _**classe**_ -
específico, que determina quais interações podemos ter com esses objetos. 

A _**classe**_ do objeto - seja ele um número, uma string ou outros mais que veremos pela frente - é o seu 'tipo'.

Deixando de lado as minhas péssimas analogias, vejamos como isso se dá em Python.<br>
Veja o seguinte programa:

```python
# Arquivo: tipos.py
print(type("Olá, mundo!"))
print(type(10))
```

Não se intimide com os termos desconhecidos. Estamos apenas instruindo o interpretador a imprimir os tipos (veja o
termo `type`) dessa string e desse número.<br>
Foque na saída do programa:

<img src="https://github.com/Neblinus/Python-LBTM/blob/b8cc5da8326a5451b46f5eb331551f4fb5aaf192/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/Tipos.png" alt="Programa Python demonstrando tipos">

O que vemos aqui são os tipos, as _**classes**_ da nossa string e do nosso número.

O que o programa nos diz é que o _tipo_, a _classe_ da nossa string é `str`, ou seja: na linguagem Python, há um
tipo, uma classe - um códon - que configura, determina - codifica - objetos (aminoácidos) do tipo `str` (string), que
representam sequências de caracteres.

De mesmo modo, na linguagem, há um tipo, uma classe - um códon - que configura, determina - codifica - objetos
(aminoácidos) do tipo `int` (do inglês _integer_, ou seja, 'inteiro'), que representam números inteiros, sem parte
fracionária.

> [!TIP]
> Números com parte fracionária são 'números com vírgula'.
> Por exemplo, se você oferece seu picolé, por educação, a um amigo, e ele devora metade do seu picolé, você é deixado com
> 0,5 picolé (meio picolé) - e com raiva dele, talvez, se fossem seus últimos R$4,00 para picolé.
> Já números inteiros não têm parte fracionária, por isso o tipo `int`, 'inteiro'.

Finalizando o conceito de tipos de dados, que será extensamente abordado nas próximas aulas, você só precisa se lembrar que,
em Python, tudo tem um tipo de dado específico, uma classe própria, que irá determinar o que pode ser feito com esse algo e
como ele interage com o programa.

Vamos avançar agora para um novo conceito.

## Literais e Variáveis
Abordarei os coneceitos de _literais_ e _variáveis_ juntos, uma vez que separá-los tornaria mais difícil sua compreensão.<br>
Dito isso, iniciemos esta última etapa da aula.

Àqueles que nunca interagiram com a área da programação antes, um detalhe pode ter passado despercebido em meio aos exemplos;
retomemos ele a seguir:

```python
# Arquivo: frases.py
print("Eu sou uma frase")
print("Eu sou uma frase" + " e eu sou outra!")
```

Nesse momento, o resultado do programa não é relevante.<br>
Reflita apenas sobre uma minúcia: _porquê digitamos `"Eu sou uma frase"` duas vezes?_

Será que não poderíamos arranjar uma forma de evitar fazer o trabalho dobrado?<br>
Qual seria a razão dessa repetição?

A resposta é simples: não temos nenhuma forma de instruir o programa a usar essa frase _outra vez_,
então, tivemos de digitá-la novamente.

---

### A especificação que faltava
Até esse momento, em todos os exemplos que vimos, usávamos `print` com algum valor entre parênteses:

```python
print("Olá, mundo!")
print(5 + 5)
print(5 + 5 - 2)
# Etc, etc, etc
```

E o programa imprimia - exibia - o valor entre parênteses, ou o resultado do cálculo - na tela do console.

Ocorre que, a esses valores que inseríamos entre os parênteses, chamamos _**literais**_.

Um _**literal**_ é qualquer valor fixo que inserimos diretamente no código-fonte e que pode ser atribuído a uma variável
(veremos logo em seguida sobre elas).

Ou seja, em um código como o seguinte, todos os valores entre os parênteses de `print` são literais, porquê foram
inseridos diretamente no código e podem ser atribuídos a variáveis:

```python
print(175)             # Literal do tipo int (inteiro)
print("Buenas noches") # Literal do tipo str (string)
print(7.5)             # Literal do tipo float (número de ponto flutuante)
print(10 * 10)         # Dois literais do tipo int (inteiro)
# Etc, etc, etc
```

Todos esses valores são considerados literais, uma vez que cumprem os requisitos para tal:
* [x] São valores fixos
* [x] Estão inseridos (digitados) diretamente no código
* [x] Podem ser atribuídos a uma variável (aguarde...)

Caso você tenha se perguntado o que seria o literal do tipo `float`, veja a definição abaixo:

> [!TIP]
> Objetos do tipo `float` representam números de ponto flutuante - uma vez que não há número fixo de algarismos
> após o ponto.<br>
> Por exemplo, poderíamos ter resultados de cálculos gerando `7.5`, `7.521`, `7.5023` ... por isso o nome `float`.<br>
> Note que, em Python, usamos o ponto (`.`) como separador, não a vírgula.

Antes de prosseguirmos para falar das variáveis, note que todos esses literais possuem um tipo, uma classe.

---

### A preguiça melhora tudo
Como seres humanos num padrão de vida estressante, num mundo (potencialmente) em colapso devido à glamourização da
_produtividade_, é normal que a preguiça seja vista como algo ruim.<br>
Nesse momento, ela será elevada ao status de _auxiliar de aprendizado_.

Retome comigo aquele exemplo que citei no início da seção de _Literais e Variáveis_:

```python
# Arquivo: frases.py
print("Eu sou uma frase")
print("Eu sou uma frase" + " e eu sou outra!")
```

Como podemos ver, usamos `print` para imprimir um literal de string, e logo após, para imprimir a soma, a junção,
a _concatenação_ (explicarei futuramente) de dois literais de string: a primeira e a segunda frase.

Agora, pense comigo: se você tivesse de escrever, num livro ou caderno, a primeira frase adicionada a uma frase aleatória,
50 vezes, você ia _mesmo_ escrever _"Eu sou uma frase"_ 50 vezes?<br>
Na verdade, você provavelmente faria isso:

> Eu sou uma frase e só queria poder dormir.<br>
> // e não comprei Nutella hoje.<br>
> // mas não sou pra ficar encarando.<br>
> ...

Se você é exemplar a ponto de perseverar ao longo de 50 frases assim, parabéns.

O que nos importa aqui é que, em programação, devemos tentar construir soluções inteligentes.<br>
Há inclusive um dizer nessa área, cuja estrutura exata não me recordo, que diz algo como:

> O difícil não é resolver problemas complexos; é não adicionar mais complexidade a eles.

Seres humanos que somos, especialmente no início da jornada de aprendizado de computação, é comum que,
por falta de conhecimento de melhores práticas ou técnicas de DSA (aprenderemos mais à frente), acabemos por
propôr soluções demasiadamente complexas para problemas que, ainda que longe de simples, poderiam ser
resolvidos com maior facilidade.

Até como pesquisadores, é difícil, muitas vezes, não se deixar levar pelo entusiasmo ou pela confiança em
uma ideia, e acabar por criar uma solução à procura de um problema.

Suponhamos que quiséssemos escrever um programa que imprimisse a frase _"Eu planto abacates"_ não 50,
mas 5 vezes - para fins de brevidade.

Uma possível solução seria esta:

```python

```

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
