# Variáveis do Shell

## Declarando variáveis

Por padrão, o nome é declarado em letras maiúsculas

~~~bash
VARIAVEL=valor
~~~

Exibindo o que foi feito:

~~~bash
echo $VARIAVEL

# valor
~~~

Na declaração das variáveis, perceba que o sinal de igualdade deve estar junto, tanto do nome da variável quanto de seu valor. Se for escrito adicionando espaços entre eles, haverá erro.

## Exportando uma variável

Quando criamos uma variável no ambiente do bash, ela fica presente apenas naquela sessão criada até que ela seja encerrada. Porém, existe a possibilidade de exportarmos uma variável para as sessões filhas da que está aberta recentemente.

Para isso utilizamos o comando `export`:

~~~bash
export VARIAVEL
~~~

Agora ao inicializarmos outra sessão que seja filha da sessão atual ela estará disponível para ela.

É possível exportar a variável já no momento de sua declaração:

~~~bash
export VARIAVEL=valor
~~~

# Adicionando o resultado de um comando dentro de uma variável

Para isso, definimos a variável seguida do comando a ser executado dentro de apóstrofos (acento grave, utilizado na crase):

~~~bash
LINUX=`uname`

# Linux
~~~

Também pode-se usar a seguinte sintaxe para obter o mesmo resultado: `DATA=$(date)`.

## Utilização de aspas no Shell

Aspas são utilizadas para proteger os caracteres para que o shell não interprete como um comando

> Utilizando \ protegemos o caractere seguinte (isso é muito utilizado com expressões regulares - regex)

### Diferenças entre aspas duplas e simples

- **Aspas duplas** protegem todos os caracteres com exceção de $, acento grave e / 

~~~bash
$, `, /
~~~

- **Aspas simples** protegem tudo, inclusive os caracteres ignorados pelas aspas duplas
