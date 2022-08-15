# Execução sequencial de comandos do shell

## Utilizando o pipe (|)

Exemplo:

~~~bash
cat alunos.txt | wc -l
~~~

	Redirecionamos a saída do comando `cat` para o comando `wc` utilizando pipe.

## Utilização sequencial

É possível fazer a execução sequencial dos comandos separando-os por ponto e vírgula (;):

~~~bash
date ; echo Linux ; ls
~~~

>> A separação acima entre os comandos e o ponto e vírgula dá-se somente em função de uma melhor visualização, nãp interfere na execução dos comandos.

## Utilizando o operadores booleanos

### &&

~~~bash
sudo apt update && sudo apt upgrade
~~~

O segundo comando só será executado caso o primeiro execute corretamente.

### ||

~~~bash
sudo apt install vlc || echo Não foi possível instalar o VLC
~~~

O segundo comando só será executado caso o primeiro apresente erro.

## Utilizando parênteses

O parênteses pode ser utilizado para executarmos um comando em um "subshell", onde podemos executar um comando sem sairmos de nosso local.

Supondo que estamos dentro no diretório textos dentro do diretório Documentos e queremos listar o conteúdo do diretório Documentos sem que para isso precisemos sair do diretório textos. Utlizando os parênteses podemos fazer da seguinte maneira:

~~~bash
(cd .. ; ls -l)
~~~

>> Note que utilizamos comando em série para isso, e não saimos do diretório atual mesmo utilizando o comando `cd ..` que retorna para o diretório superior.
