# Adicionando comentários - boas práticas

Um bom script deve ser bem comentado para facilitar o seu próprio entendimento futuro como também o de outra pessoa que precise lê-lo.

Para boas práticas nos comentários, algumas regras devem ser seguidas.

1. **Cabeçalho**

O cabeçalho deve ter informações como:
- para que serve o script
- quem criou o script
- data de criação
- quais alterações criadas

~~~bash
#####################################################
#
# Primeiro script.sh - Script de Exemplo do Curso
#
# Autor: Thiago Souza (tjbass2013@gmail.com)
# Data Criação: DD/MM/AAAA
#
# Descrição: Script de exemplo que lê data e hora e exibe a lista de alunos
#
# Exemplo de uso: ./primeiroScript.sh
#
# Alerações:
#    Dia X - inclusão da função de ordenação
#    Dia Y - correção da função de leitura
#####################################################
~~~

2. **Descreva funções complexas**

Antes de uma função mais complexa, é uma excelente prática comentá-la. Evite sempre comentários de trechos óbvios, como também poluir o código com tantos outros comentários inúteis que falam o que está evidente. Foque em comentar linhas mais complexas que realmente necessitam de uma explicação quanto a sua funcionalidade.
