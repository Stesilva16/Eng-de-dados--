<h1>Redes : Introdução a redes de computadores</h1>



<h2>Qual a função do engenheiro de dados?</h2>

O engenheiro de dados é responsável por coletar, armazenar, processar e analisar grandes quantidades de dados para extrair informações úteis e tomar decisões informadas. Eles usam tecnologias como Big Data, machine learning e inteligência artificial para transformar dados brutos em insights valiosos para a empresa ou organização. Eles também são responsáveis por garantir a integridade e a segurança dos dados e desenvolver sistemas e processos para automatizar a coleta e o processamento de dados.

<h3>Introdução Infraestrutura</h3>

Infraestrutura de redes é o conjunto de equipamentos, tecnologias e procedimentos que formam a base para a transmissão de dados em uma rede. Isso inclui dispositivos como switches, roteadores, firewall, cabos e outros componentes. A infraestrutura de rede é responsável por garantir que os dados sejam transmitidos de forma segura e eficiente entre os dispositivos conectados, permitindo que os usuários compartilhem informações e acessem recursos compartilhados com facilidade. Além disso, a infraestrutura de rede também é responsável por monitorar e garantir a disponibilidade da rede, bem como proteger contra ameaças de segurança cibernética.

Pontos relevantes sobre Infra:

- 1- Faz a tradução de ip/http e visse-versa: **Servidor DNS**
- 2- DNS é o serviço padrão da internet, que faz especificamente a transferência de msg de texto: **Falsa, quem faz é o HTTP**
- 3- qual protocolo faz os computadores obterem endereço IP automaticamente e diretamente colocado no roteador de maneira ativa: **DHCP**
- 4- Carrega o endereço fixo, geralmente imutável de um disp de rede: **MAC**
- 5- Nome que se dar a conexão de rede entre dois países: **Internet**
- 6- A ARPANET foi o único modelo anterior à internet: **Errada**
- 7- É responsável por “controlar” e distribuir de forma automatizada as configurações de rede em um conexão e geralmente é uma função que está presente no roteador: **DHCP**
- 8- Sistemas responsáveis por conectar nossos dispositivos com a internet de maneira ampla: **ISP**
- 9- Topologia de REDE: **Desenho para um entendimento da rede**
- 10- Modelo utilizado em massa nas redes mundiais: **Estrela**
- 11- O gatway funciona como uma ponte que interliga dois ip’s numa mesma rede: **falso (interliga dois ip’s em redes diferentes)**
- 12- Problema causado pela distância entre a requisição do dado pelo cliente e o servidor que o dado se encontra: **Delay**
- 13- Quando um servidor ou serviço está sobrecarregado ou o meio de transmissão apresenta falhas de congestionamento o problema ocorre e pode ser percebido em transmissão em “tempo real”, falamos de: **Jitter**
- 14- É o principal meio de transmissão de redes, devido a não sofrer interferência eletromagnética e conseguir transmitir uma altíssima largura de banda: **Cabo de Fibra Ótica**
- 15- comumente utilizado em uma rede de dados. Esse meio é utilizado devido a sua maleabilidade e custo beneficio mas pode sofrer interferência eletromagnética: **Cabo UTP**

<h3>Hardware e Redes</h3>

Hardware é o conjunto de componentes físicos que compõem um computador ou outro dispositivo eletrônico, como processadores, memórias RAM e ROM, discos rígidos, placas-mãe, placas de vídeo, placas de som, unidades de CD/DVD, dispositivos de entrada (teclado, mouse, scanner, etc.), dispositivos de saída (monitor, impressora, alto-falantes, etc.), entre outros. Estes componentes trabalham juntos para realizar tarefas específicas e processar informações. Já a rede é um conjunto de dispositivos interconectados que permite a comunicação de dados entre computadores e dispositivos eletrônicos. Ela pode ser utilizada para compartilhar recursos, como impressoras, armazenamento de dados, aplicativos e acesso à Internet. As redes podem ser classificadas em diferentes tipos, como LAN (Local Area Network), WAN (Wide Area Network) e WLAN (Wireless Local Area Network), dependendo da sua escala e alcance geográfico. A infraestrutura de uma rede inclui cabos, roteadores, switches e firewalls, que garantem a segurança e o desempenho da rede.

Pontos relevantes:

- - cache - Auxilia o processador ao executar os processos do pc, diminuindo o gargalo entre memória RAM e Processador.
- falamos sobre os componentes de hardware, passamos por HD ou SSD, placa de vídeo, processador, placa mãe, memória RAM e dispositivos de entrada e saída.

- Conexão de rede - só existe uma rede quando há dois ou mais dispositivos conectados e trocando informações
- MAC - obrigatório para se entrar em rede e único e insubstituível. (se compara a um CPF)
- O MAC obtém as configurações necessárias para acessar a rede, são 4 informações:
  - IP - é o endereço de referência do dispositivo, geralmente randômico. existem 2 versões atualmente:
    - IPv4 - vai de 0.0.0.0 à 255.255.255.255
    - IPv6 - vai do 0.0.0.0 ao F.F.F.F
  - Mascara - Ela mascara a rede, como o próprio nome já diz.
    - IP privado são divididos em redes locais
    - IP’s públicos são utilizados na rede comum.
  - Gateway - ele é a rota, determina as pontes de entrada/saída da rede. Em 99,99% dos casos ele é o próprio roteador.
  - DNS - é um tradutor que faz a tradução entre domínios e IP’s. exemplo:
    - domínio = [www.google.com](http://www.google.com/) > DNS traduz > IP = 255.255.255.255
    - É possível acessar um endereço na rede, mesmo sem o DNS, sabendo o IP do endereço que você quer acessar, não precisa de tradução e consequentemente não precisa do DNS.
    - Para saber o IP de um endereço basta fazer o teste no cmd. ex: ping [www.google.com](http://www.google.com/), isso vai me retornar o IP da google além do teste de latência.

- Mascara - Ela mascara a rede, como o próprio nome já diz.
  - IP privado são divididos em redes locais
  - IP’s públicos são utilizados na rede comum.
- Dentro dos IP’s públicos (válido), foi reservado uma faixa de IP’s para seja utilizado como privado (não válido), essas faixas são:
  - 10.0.0.0 - 10.255.255.255
  - 172.16.0.0 - 172.31.255.255
  - 192.168.0.0 - 192.168.255.255
- O dispositivo que faz essa gerência dos IP’s é o roteador e qualquer IP que não estiver nas faixas indicadas acima, são IP’s públicos.
- Toda vez que o computador retornar a faixa especial 169.254, significa que você não está conectado a nenhuma rede, somente a si próprio.
- A mascara tem o padrão: 255.255.255.0 e dentro da rede, só é possível utilizar o mascaramento de até 253 dispositivos (padrão), o mascaramento funciona como uma subtração e por padrão são guardados dois IP’s, um para o próprio roteador (geralmente o primeiro) e o último (ex: 192.168.0.255) que é utilizado como Broadcast, que serve para descobrir quantos e quais os IP’s privados/dispositivos que estão presentes na rede.
- Quando eu limito a minha mascara (colocando um número ao final, ex: 255.255.255.100) eu estou limitando minha rede à 255-100-2 dispositivos, ou seja, a 153 dispositivos.

- Se eu quero limitar a quantidade de dispositivos eu uso o último octeto da mascara, se eu quero aumentar a quantidade de computadores, ou seja, criar sub-redes, nós alteramos os outros octetos. Exemplos:
  - 255.255.255.0 = 253 ips
  - 255.255.254.0 = 253 * 2 ips = 506 ips
  - 255.255.251.153 = (255 - 153 - 2) * (255 - 251 + 1) = 100 * 5 = 500 ips
- CIDR - é uma abreviação da máscara, onde o /24 corresponde a máscara padrão 255.255.255.0, já o CIDR /32 corresponde à mascara 255.255.255.255, ou seja, totalmente fechada e 0.0.0.0 ao CIDR /0 o menor, que corresponde a máscara da internet.

- Entramos nos tipos de computadores e SO (sistemas operacionais)
- O que são servidores: são máquinas dedicadas ao fornecimento de serviços e processamento de operações à um cliente e garantir a disponibilidade desses serviços.
- Arquitetura Cliente x Servidor
- Localização dos servidores:
  - Servidores locais (On Premise)
  - Servidores em nuvem (Cloud)
- Introdução à Cloud computing e a relação entre Nuvem pública x nuvem privada.

- Tipos de servidores:
  - ***\*Servidor de aplicação -\**** é onde temos uma aplicação e ele é disponibilizado para outros dispositivos dentro da empresa
  - ***\*Servidor de Arquivos -\**** exemplo Google drive
  - ***\*Servidor de banco de dados -\**** mySQL
  - **Servidor de mídia -** Netflix, Amazom
  - ***\*Servidor de email -\****
  - ***\*Servidor FTP -\**** File Transfer Protocoll
  - ***\*Servidor Proxy -\**** Serve para controle de tráfego do usuário,
  - ***\*Servidor Web -\****