# Exit Code

O `exit code`, ou códido de retorno, consiste em um número que varia de 0 a 259, sendo 0 sempre um retorno de sucesso. Qualquer número diferente de 0 é um tipo de erro que está definido na documentação do comando em questão. 

É possível consultar o `exit code` no manual do respectivo comando, embora alguns não possam contar com essa informação.

Para consultar o determinado `exit code` de um comando, após a sua execução, basta digitar o comando `echo $?` que o valor será exibido no terminal.

Em um script é possível utilizá-lo como os demais comandos, apenas o colocando na sequência do comando anterior do qual se quer obter esta informação.

~~~bash
#!/bin/bash

ls /home/thiago

echo $?
~~~

Uma forma mais eficiente, principalmente quando se está trabalhando com scripts longos, é vincular os `exit codes` dos comandos que se quer monitorar à variáveis específicas.

~~~bash
#!/bin/bash

ls /home/thiago

RETURN_CODE_LS=$?

echo "O código de retorno do ls foi $RETURN_CODE_LS"
~~~

**PS**: também é possível exibir o `exit code` de um comando executado a partir de um script utilizando o comando `exit`.

~~~bash
#!/bin/bash

ls /home/thiago

exit $?
~~~


