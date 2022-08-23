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
