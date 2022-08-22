# Nomes, permissões e execução do script

- A primeira linha escrita no script deve ser a indicação de qual será o interpretador deste script:

~~~bash
#!/bin/bash

# --- resto do script ---
~~~

Em um script simples, basta escrever os comandos em sequência que eles serão executados normalmente. Por exemplo:

~~~bash
echo "Isto é um simples script shell"
sudo apt updade && sudo apt upgrade -y
# Acima, o comando para atualizar o sistema
# E comentários podem ser adicionados utilizando o jogo da velha
~~~

Para executar um script podemos utilizar o `./`, que diz para o interpretador o caminho para execução script. Esse comando é equivalente a indicar no terminal o caminho completo do script.

~~~bash
./ primeiro_script.sh
~~~
