# Usando variáveis no script

A utilização de variáveis dá-se em razão de:
- Facilita a leitura do código;
- Uso para valores que possam ser alterados;

## Sintaxe na declaração de variáveis

~~~bash
VARIAVEL=$(date +%H:%M)
~~~

## Chamando a variável

~~~bash
echo "Hora atual: $VARIAVEL"
~~~

> Normalmente, todas as variávels são declaradas no começo do código.

É possível redeclarar uma variável e atribuir a ela um novo valor. Isso irá sobrescrever a variável de mesmo nome criada anteriormente.

As variáveis não precisão ter seu tipo definido, ou seja, no shell script sua tipagem é dinâmica.
