 # Trabalho* realizado na Semana #4

## tarefa 1
  (comandos na bash)

## tarefa 2

  - passo1: observamos que guardou no file os valores das variáveis ambiente do processo-filho.
   
- passo2:  observamos que guardou no file2 os valores das variáveis ambiente do processo-pai.

- passo3: Usando o comando "diff"  para os dois ficheiros verificamos que os dois ficheiros output são iguais. Ou seja, todas as variáveis ambiente do processo-pai foram passadas para o processo-filho.

## tarefa 3

- passo1: Não houve qualquer output.

- passo2: Imprimiu as variáveis ambiente.

- passo3: A variável environ é um array de de strings que contém as variáveis ambiente na forma "nome da variável" = value. Assim, alterando a chamada para "execve("/usr/bin/env",argv,environ), e subtituindo NULL por environ obtemos o output pretendido.

## tarefa 4
 
 - o programa imprime todas as variáveis ambiente em /usr/bin/env. Ou seja, a função system passou as variáveis ambiente para /bin/sh.
  

## tarefa 5




- O PATH e variável ambiente que escolhemos foram definidas e printadas, mas LD_LIBRARY_PATH não foi printado,ou seja, significa que não foi passado para o processo-filho. 

- Concluimos que se um usuário definir a variável ambiente LD_LIBRARY_PATH e invocar um programa set-UID, o programa omite a 
a variável ambiente, a não ser que o usuário seja dono do programa.


## tarefa 6

- O programa irá correr o nosso código em vez de executar /bin/ls
  O código irá correr como root priveligeado isto porque mudámos o seu dono para o root.

- a variável ambiente PATH procura pelo comando ls no diretório corrente. Quando ele encontra o "ls" é executado o nosso programa em vez do comando da shell.

- programas set-UID conseguem correr ficheiros maliciosos com privilégios de root se a variável ambiente PATH for alterada.





