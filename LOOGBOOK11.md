# Tarefa 1

Nesta tarefa geramos um certificado autoassinado , ou seja uma entidade confiável que emite certificados digitais. 

1)Parte do certificado que garante que este é um certificado CA:  
![fig1](1.png) 

2)Trata-se de um certificado autoassinado, uma vez que o Subject é igual ao Issuer:
![fig2](2.png)

3) No RSA Algorithm temos um expoente publico e; ![fig3](3.png)  
um expoente privado d; ![fig4] (4.png) 
modulus n; ![fig5](5.png)
p -> prime1 ![fig6](6.png)
q -> prime2 ![fig7](7.png)

# Tarefa 2

Nesta tarefa pretende-se gerar um CSR, este será gerado então pelo CA criado correndo o seguinte comando: 
![fig8](8.png)

Corremos de seguida o seguinte comando para podermos permitir ter nomes alternativos 
![fig9](9.png)

![fig10](10.png)

# Tarefa 3

Primeiramente transformamos a solicitação de assinatura de certificado em um certificado X509 usando o seguinte comando: 
![fig11](11.png)

Depois descomentamos o "copy_extensions" do ficheiro openssl.cnf e de seguida usamos o seguinte comando para imprimir o conteudo descodificado do certificado:

![fig12](333.png)
![fig13](334.png)











