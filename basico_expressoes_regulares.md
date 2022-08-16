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

*Exibindo linhas em branco*
 
 Para isso, usamos o comando `egrep "^$"`
## Uso dos caracteres especiais

**\*\**: como dito acima, seu uso difere do fileglobbing. 

Exemplo:

~~~bash
egrep "b[a-i]g*" texto.txt
~~~

O comando acima exibirá todo o conteúdo que contenha a regra especificada antes do asterisco - com a diferença de que com o uso file globing seria mostrado sempre as situações em que b**g apareceriam de forma sequencial, porém, com o asterisco nas empressões regulares é considerada tbm a não ocorrência também de algumas delas.

Ou seja: a definição é que a letra anterir ao asterisco na regex pode existir ou não.

**+**: define que o caractere anterior precisa aparecer ao menos uma vez.

~~~bash
egrep "b[a-i]g+" texto.txt
~~~

**?**: define que o caractere anterior pode aparecer nenhuma ou apenas uma vez.

~~~bash
egrep "b[a-i]g?" texto.txt
~~~

**.**: define que será exibido apenas o conteúdo que contenha qualquer caractere entre o primeiro e o segundo termo especificados.

~~~bash
egrep "O.Linux" texto.txt

# O comando acima exibirá apenas a linha que contenha um único caractere entre o O e Linux.

# Como o ponto representa um caractere, se quisessemos exibir um conteúdo com mais de um caractere entre os termos, usaríamos mais de um ponto em sequência.
~~~

Combinando o ponto com o asterisco podemos ter um resultado complexo bastante interessante. 

Para definirmos o retorno do conteúdo que comece especificamente com o O e que termine com a palavra Linux, independente da quantidade de caracteres entre os dois termos, usamos:

~~~bash
egrep "O.*Linux" texto.txt
~~~

