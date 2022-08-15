# Básico de expressões regulares

## Diferença entre o `grep` e o `egrep`

A diferença entre o `grep` e o `egrep` é que o segundo aceita mais expressões regulares, pois se trata de umaversão extendida do primeiro.

Equivalente ao `egrep` é o comando `grep -e`

## Usando o egrep com expressões regulares

~~~bash
# o comando a seguir:
egrep "[Li]inux" texto.txt
# está procurando dentro do arquivo `texto.txt` as ocorrências da palavra Linux, seja com inicial maiúscula ou minúscula
~~~

*Retornando todas a linhas que começam com uma determinada palavra*

~~~bash
egrep "^Linux"
~~~

> NOTE o uso do `^` antes da palavra especificada.

Ao utilizarmos a flag `-v` junto do comando egrep teremos o efeito reverso do comando acima, ou seja, haverá o filtro a partir da exclusão das linhas que inicializem com a palavra Linux, consequentemente tendo a exibição dos demais conteúdos do arquivo.

~~~bash
egrep -v "^Linux"
~~~

*Filtrando a exibição ao encontrar o conteúdo apenas ao fim da linha*

~~~bash
egrep "Linux$"
~~~

> NOTE agora que foi adicionado o `$` na sequência da palavra Linux.
