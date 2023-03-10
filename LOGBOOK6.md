# Tarefa realizada na semana #6


## tarefa 1

 Uma maneira que achamos que poderia funcionar para crashar o programa seria ao 
   substituir na função myprintf() o printf(msg) por printf("%s%s%s%s%s%s%s%s%s%s%s%s").
          Para cada %s, a funcao printf() irá buscar um número da stack, tratar desse número como um endereço e printar o que contém na memória apontada por esse endereço como uma string,
          ate um endereço NULL ser encontrado.        
            Como o número trazido pelo o printf() pode nao ser um endereço, a memoria apontada por    esse número pode nao existir e assim o programa ira crashar. 
              
          
          
