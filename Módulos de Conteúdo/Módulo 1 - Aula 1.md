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

---

### Dados para todos
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

Em Python, tanto as strings que vimos como os números são _objetos_, ou seja, um identificador (ID) interno associado a um endereço
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
mas 5 vezes - para fins de brevidade.<br>
Vejamos o que faríamos nessa situação.

### Ao vencedor, os abacates
Vamos explorar o último tópico seguindo esse exemplo simples, para o problema dos abacates - também simples.

Uma possível solução seria esta:

```python
print("Eu planto abacates.")
print("Eu planto abacates.")
print("Eu planto abacates.")
print("Eu planto abacates.")
print("Eu planto abacates.")
```

Mas ela não me parece a mais eficiente - e, obviamente, se chegamos nesse ponto, _você_ já sabe que teremos
uma solução melhor.

O que usaremos para solucionar esse problema é uma capacidade fundamental dos computadores: _armazenar dados_,
ainda que temporariamente.

Para aqueles com baixa familiariedade com computação, os computadores são dotados de dispositivos de memória
RAM, que vem do inglês _Random Access Memory_, ou Memória de Acesso Aleatório. Através deles, podemos armazenar
e acessar dados de forma extremamente rápida, tendo esses deletados durante o tempo de execução do sistema
operacional (a depender do tempo de vida de um processo ou aplicação) ou após o encerramento desse sistema.

<details>
  <summary>Curiosidade sobre a memória RAM</summary>
  <p>Ainda que, em geral, os dados na RAM sejam destinados à execução de programas e processos, e sejam deletados
  quando se interrompe o fornecimento de energia elétrica para o dispositivo de RAM - quando se desliga o computador
   - algumas técnicas de perícia computacional permitem a recuperação de dados mesmo desses dispositivos de memória
  volátil.</p>
</details>

Desse modo, vamos arranjar uma forma de 'guardar' e acessar nossa frase _"Eu planto abacates"_).

Para isso, reflita comigo: se você tem, por exemplo, 3 filhos, e você quer que apenas um deles venha até a sala,
o que você faz?

Você o chama pelo nome, que irá então lhe dar acesso ao _valor_ a qual o nome está ligado - pobre Enzo, sempre
aprontando.

Uma variável é exatamente como Enzo - não fazendo bagunça na casa inteira, mas sim, um _identificador_ com um valor
_atribuído_ a ele. Ao termos essa estrutura (um identificador associado a um valor), podemos constantemente 'chamar'
esse identificador e acessar seu valor, para fazer seja lá o que precisamos de fazer com ele.

Como isso se dá em Python? De forma simples: usando o _operador de atribuição_, que nada mais é que um símbolo pré-definido
que mostra ao interpretador Python que _estamos ligando um valor a um identificador_, uma variável.

Observe:

```python
# Arquivo: variavel.py
meu_numero_favorito = 7
print(meu_numero_favorito)
```

O resultado desse programa, naturalmente, é:

<img src="https://github.com/Neblinus/Python-LBTM/blob/0fa4d40d64fd9a3f56c5b107d1ebd8c5b0902e20/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/Variavel.png" alt="Programa Python demonstrando variáveis">

Nesse programa, temos a lógica básica das variáveis em funcionamento:

* Definimos um identificador, nesse caso, `meu_numero_favorito`
* Inserimos o _operador de atribuição_, um símbolo de 'igual' (`=`)
* Inserimos o valor a ser atribuído a `meu_numero_favorito`, nesse caso, `7`

Assim, temos que o interpretador Python selecionou uma região da memória e associou-a ao identificador
`meu_numero_favorito`, e logo após, realizou a operação definida pelo operador de atribuição (`=`), ou
seja, tomar um valor à sua direita (nesse caso, o literal de tipo `int` `7`) e atribuí-lo à variável à
esquerda.

Desse ponto em diante, todas as vezes que o programa tiver `meu_numero_favorito` inserido em algum trecho
de código, ele acessará seu valor e obterá, nesse cenário, o `int` `7` (ou algum outro valor, caso a variável
tenha sido atribuída a algo diferente ao longo do programa...mas isso, deixemos para depois).

Voltando ao exemplo dos abacates, teríamos a versão melhorada assim:

```python
# Arquivo: abacate.py
frase_repetida = "Eu planto abacates."
print(frase_repetida)
print(frase_repetida)
print(frase_repetida)
print(frase_repetida)
print(frase_repetida)
```

E como resultado:

<img src="https://github.com/Neblinus/Python-LBTM/blob/47a8f1c44af303974cdbc4525cf2c6daf6e0843c/M%C3%B3dulos%20de%20Conte%C3%BAdo/Imagens/Abacate.png" alt="Programa Python demonstrando variáveis">

> [!NOTE]
> Ainda veremos como nos livrar da repetição de `print`s.<br>
> Para os curiosos, tem a ver com loops...

E assim, concluímos a primeira aula.<br>
Esses tópicos todos serão ainda largamente abordardos ao decorrer das aulas, junto a muitos outros que iremos
aprender.

---

#### Um pequeno adendo
Isso ainda será explicado futuramente em detalhes, mas para quem quiser saber, em programação, temos linguagens
de tipagem estática e dinâmica.

Linguagens de tipagem estática tem funcionamento organizado de modo que as variáveis não possam mudar de tipo ao
longo da execução do programa, por meio de declarações explícitas e checagens do compilador, dentre outros mecanismos.

Por exemplo, numa linguagem estática como Java:

```java
public class OlaMundo
{
  public static void main(String[] args)
  {
    String saudacao = "Olá, mundo!";
    System.out.println(saudacao);
  }
}
```

Não se preocupe em entender essa linguagem; ela não é nosso foco.<br>
O programa acima define uma variável do tipo `String` (note a linha iniciando em `String`), com um literal
atribuído a ela (`"Olá, mundo!"`), e imprime seu valor na tela.

Uma vez declarada, a variável `saudacao` não poderá mudar de tipo: só poderá armazenar strings.

Compare com a versão em Python desse programa:

```python
saudacao = "Olá, mundo!"
print(saudacao)
```

Como podemos notar, não há, por exemplo, uma declaração `str` antes do nome da variável `saudacao`.<br>
Isso ocorre porque Python possui tipagem dinâmica, ou seja, o tipo da variável pode, sim, mudar durante a
execução do programa.

As implicações de cada abordagem discutiremos mais à frente; por ora, saiba que tipagem estática e dinâmica
existem!

> [!NOTE]
> Falaremos mais à frente sobre inferência de tipos também.

**Obrigado por ter lido, até a próxima!**
