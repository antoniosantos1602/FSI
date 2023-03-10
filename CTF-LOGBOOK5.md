# DESAFIO 1

No código main.c, percebemos que o programa abre e lê o ficheiro mem.txt que está definido por **char meme_file[8]**. O nosso objetivo neste primeiro desafio era provocar um buffer overflow e conseguir abrir o ficheiro flag.txt em vez do mem.txt.

Tendo um **char buffer[20]** na stack a seguir ao **char meme_file[8]** sabíamos que fornecendo mais de 20 bytes na leitura do buffer (via scanf) conseguíamos escrever no campo meme_file, controlando assim o ficheiro que era aberto e abrindo aquele que nós desejávamos. Assim fizemos, fornecendo ao scanf a string aaaaaaaaaaaaaaaaaaaaflag.txt.

Ocorreu o overflow e fomos capazes de obter a flag.

# DESAFIO 2

Neste desafio, foi introduzido um mecanismo de combate ao exploit utilizado no desafio anterior, estando na stack entre o meme_file e e o buffer um **char val[4]**. Antes de abrir o ficheiro, o programa verifica se o valor de val se mantém igual ao valor inicialmente definido. Se não se mantiver, significa que houve ouverflow do buffer e o programa não inicia a execução normal, enviando em vez disso uma mensagem de erro.

Esta alteração no código mitiga a facilidade na exploração do exploid mas pode, na verdade, ser facilmente ultrapassada. Para isso, é preciso fornecer ao programa aquando do scanf 20 bytes que preenchem o buffer, 4 bytes que preenchem o val e o "flag.txt" que coloca na posição meme_file o valor do ficheiro que queremos que o programa abra. No entanto, para que o programa inicie a rotina normal, precisamos de colocar no campo do val um valor igual ao que está inicialmente definido (0xfefc2122). Contudo, como a alocação de inteiros em memória é feita com little endian, este valor deve ser fornecido num formato próprio (\x22\x21\xfc\xfe). Assim fizemos, fornecendo ao scanf a string aaaaaaaaaaaaaaaaaaaa\x22\x21\xfc\xfeflag.txt.

Para facilitar a solução deste problema, usamos o script em python fornecido no desafio 1. Ocorreu o overflow e fomos capazes de obter a flag.
