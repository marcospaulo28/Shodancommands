# ShodanDorks
A brief summary of how to exploit Shodan's OSINT technology and Dorks Commands.
1. BUSCA SIMPLES
No campo para preencimento de busca você pode fazer a busca de termos como o nome do servidor, por exemplo: Apache, Nginx, etc.
As informações de cada serviço são armazenadas em um objeto chamado banner . É a unidade fundamental de dados que Shodan reúne
SOBRE o que você estará procurando. Você também pode procurar por dispositivos, por exemplo: Moxa Nport.

2. REFINANDO A BUSCA (Utilizando os comandos Dorks)
Para refinar a busca você pode usar Filtros de Pesquisa: filtername:value, country:BR onde as duas letras maiúsculas representam um pais
especifico.
Tambem podemos procurar por uma rede de uma organização específica dentro de uma cidade: org:"SingTel Mobile" city:Singapore.
OBS: QUANDO FOR UM NOME COMPOSTO UTILIZA AS "ASPAS DUPLAS"
<!-- Outro filtro de pesquisa é PORTA --> Exemplo country:BR port:80 obs:A porta 80 é normalmente para páginas da web que não são criptografadas.
Podemos pesquisar por Produto usando o filtro Ex: product:"Counter-Strike Global Offensive" , para os servidores do jogo Online Counter Strike

SOBRE AS PORTAS:
Porta 20 (UDP) - abriga o File Transfer Protocol (FTP) usado para transferência de dados
Porta 22 (TCP) - abriga o protocolo Secure Shell (SSH) para a segurança de logins, FTP e encaminhamento de porta
Porta 53 (UDP) - abriga o Domain Name System (DNS), que transforma nomes de domínios em endereços IP
Porta 80 (TCP) - abriga o HTTP da rede mundial de computadores
Porta 5432(TCP) -	PostgreSQL database system

3. PARA SERVIDORES INFECTADOS COM RAMSONWARE
has_screenshot:true encrypted attention

4. BUSCA POR WEBCAMS
Utilizar Server + designação do tipo de camera Ex: Server: SQ-WEBCAM

5. REMOVENDO TERMOS
 -> Este é um operador lógico que remove resultados que contenham determinada palavra. Exemplo: -authentication
NOT -> Este operador lógico possui a mesma função do operador anterior. Example: NOT authentication

6. BUSCA DE SISTEMAS OPERACIONAIS
Por exemplo: os:"Windows 7" city:"São Paulo"

7. INSTALANDO SHODAN NO UBUNTU
apt-get update
apt-get install python-pip
pipe install shodan
shodan init "chave API"

8. REALIZANDO BUSCAS COM SHODAN NO TERMINAL LINUX
shodan count |sitema operacional + versão|
shodan count |tipo de servidor web, apache, nginx, etc
shodan search nginx --limit 10 "abre a lista de servidores encontrados.
shodan host |IP| para 1 servidor específico
