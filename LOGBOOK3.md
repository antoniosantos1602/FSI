# Trabalho realizado na Semana #3

## Identificação

- O stack do protocolo TCP/IP do Windows (IPv6) lida de forma inapropriada com um pacote de Router Advertisement no Neighbour Discovery Protocol.
- A chegada de um pacote com um número par de conjuntos de 8 bytes ao campo Length do Recursive DNS Server leva a um buffer overflow.
- O utilizador fica com um Blue Screen of Death e fica permitida a execução de código à distância (RCE).
- Todas as versões do Windows 10 e Windows Server 2019 com configuração default podem estar vulneráveis.

## Catalogação

- O reporting desta vulnerabilidade foi feito diretamente pela Microsoft quando a descobriu, a 13 de Outubro de 2020.
- O nome Bad Neighbor foi-lhe dado pela McAfee por estar relacionada com o Neighbor Discovery Protocol.
- O nível de gravidade atribuído foi de 8,8.


## Exploit

- Para explorar esta vulnerabilidade , o atacante tem de estar no mesmo segmento de rede que as suas vítimas.
- Um script que leve a um buffer overflow do  campo Length do RDNSS pode ser usado para explorar a vulnerabilidade.
- A exploração bem-sucedida desta vulnerabilidade requer o envio de pacotes de ICMPv6 Router Advertisement, especialmente criados para um computador Windows remoto.

## Ataques

- Não são conhecidos ataques usando esta vulnerabilidade.
- A Microsoft desaconselha a desativação do IPv6 mas sugere a desativação da opção RDNSS.
