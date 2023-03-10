# CTF para a semana #4

- desafio1 : Navegando pelo o servidor de Wordpress, recolhemos algumas informações pertinentes como a versão do wordpress(5.8.1), Woocommerce plugin(5.7.1), Booster for WooCommerce plugin(5.4.3)...

  O ponto crucial na descoberta da CVE foi a review encontrada no produto "WordPress Hosting" em que o cliente se queixava das atualizações dos plugins do Wordpress.

   

  Percebemos assim que para encontrar a CVE desejada poderíamos experimentar pesquisar CVE's relacionadas com a versão das atualizações dos plugins(Booster for WooCommerce plugin(5.4.3)) num motor de busca de CVE's.









- desafio2: Depois de encontrado a CVE do desafio 1 para encontrar o  exploit para a CVE, pesquisamos no exploit database(www.exploit-db.com/search) pela CVE econtrada no desafio 1, onde se encontrava um código python que representava a exploit.

    Ao compilar e executar o programa na forma: "python3 exploit.py /http://ctf-fsi.fe.up.pt:5001 1" (1 como administrador) foi nos apresentado na shell 3 links para entrar como administrador.
    
    Ao clicar no primeiro link, conseguimos encontrar o post privado que continha a flag pretendida.
  
