# Recebendo entrada do usuário

Para receber dados do usuário podemos usar o comando `read`.

Sintaxe:

~~~bash
read VARIAVEL
~~~

A partir daí o shell ficará aguardando que o usuário digite algo para que seja registrado.

É possível declarar mais de um valor a mais de uma variável ao mesmo tempo:

~~~bash
read VAR1 VAR2 VAR3

# aqui será recebido na sequência em que for digitada no shell separados por espaço.
~~~

## Exibindo texto no prompt com o read

Para exibir uma mensagem para o usuário com o uso do comando `read` ao invés de `echo` enquanto ele recebe dados do usuário, utiliza-se a flag `-p`

~~~bash
read -p "Digite seu nome: " NOME
~~~

Neste caso, o prompt para recebimento ficará exatamente na sequência da frase, na mesma linha, ao contrário do comando `echo` que acontecia uma quebra de linha dada a sequência de execução dos comandos.

## Omitindo a inserção do usuário na tela

Para fazer a omição do texto inserido pelo usuário na tela, utiliza-se a flag `-s`. Essa opção é útil quando se nencessita a digitação de uma senha.

~~~bash
read -s SENHA

# Durante a digitação do usuário, nada será exibido
~~~

# Recebendo entrada de usuários de parâmetros

No shell parâmetros de um comando são os valores digitados após ele separados por espaços.

Exemplo:

~~~bash
evince document.pdf
~~~

Acima, o parâmtro do comando `evince` é document.pdf,

Em um script os parâmetros podem ser verificados da seguinte maneira:

~~~bash
# $0 - Nome do parâmetro
# $# - Quantidade de parâmetros
# $* - Todos os parâmetros
# $1-9 - Cada um dos parâmetros

echo "O script $0 recebeu $# parâmetros."
~~~
