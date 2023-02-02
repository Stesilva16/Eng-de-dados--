<h1>Cloud Computing</h1>



<h2>O que é o Cloud Computing?</h2>

Cloud Computing é uma tecnologia que permite acesso a serviços de TI pela internet, oferecendo recursos de computação, armazenamento e outros serviços em nuvem. Isso significa que, em vez de instalar e gerenciar softwares e equipamentos em seus próprios servidores, você pode acessar esses recursos remotamente através da internet. Isso oferece vantagens, como economia de custos, escalabilidade, flexibilidade e acessibilidade.

<h3>Pontos relevantes</h3>

- É um serviço de computação na nuvem que utiliza recursos de TI sob demanda, permitindo que você pague apenas pelo que consome.
- É para todos, oferecendo liberdade para montar sua máquina ou rede de acordo com suas necessidades.

- É ilimitado, pois é quase impossível usar todos os recursos de um provedor de nuvem.

- Redução de custos
- Sem manutenção
- Escalabilidade quase ilimitada
- Alta confiabilidade

- Nuvem Pública: oferece redução de custos, sem manutenção, escalabilidade e alta confiabilidade.

- Máquina Virtual é uma emulação de hardware.

- Com o Serverless Computing o usuário não precisa se preocupar com a infraestrutura da rede, que é feita de forma autônoma pelo provedor de nuvem.

- Big Data: Ferramentas robustas (Dataflow, Pub/Sub, Dataproc) que podem ser configuradas rapidamente.

<h3>GCP: pontos importantes</h3>

- A nível geral, todos os projetos têm um Id único.

- Todo faturamento é feito a nível de projeto.

- Dica: **nome do projeto:** pode ser alterado de forma a ter duplicatas mas os nº de projeto e Id são únicos.

- Google Cloud status → mostra o status de todos os serviços da plataforma.

- Dentro do Google Cloud ele não chama pela solução e sim pelo nome do serviço. Ex: Vm’s ele chama de Compute Engine e na AWS é EC2.

- O shell, te permite alocar até 10Gb de espaço disponível de forma gratuita automaticamente.

- Azure, AWS e GCP -

   

  IAM

   

  tem o mesmo nome da solução.

  - Não existe projeto sem proprietário
  - papéis = regras (roles)
  - Dentro da empresa, nunca deixe alguém com o mesmo nível de hierarquia de projeto, sendo como proprietário.
  - Tem três principais e dai a gente vai organizando de acordo com a necessidade, sendo eles, administrador, redator ou leitor.

- Criando um novo projeto, é possível alterar o nome do projeto, mas não é possível editar o ID do projeto pois ele é único no mundo.

- Todos os nomes de atribuição dentro do GCP não é possível utilizar letras maiúsculos e caracteres especiais diferentes do hifens. Segue uma padronização de infraestrutura multicloud.

- A nível de organização, o GCP acompanha o nível de hierarquia de pastas, que se aproximam do conceito de grupos e dessa forma é possível organizar os times que trabalham em cada projeto e quais os recursos que esse time irá consumir além de ter o controle de gastos e promover a segurança de informações sensíveis entre setores da empresa dentro do ambiente Cloud.

- Configurações de Billing (Faturamento), realizar a criação de Budgets e alerts (Orçamentos e alertas) para ter o controle financeiro das atividades na plataforma.

<h3> Máquinas Virtuas (VM)</h3>

- Montando uma nova VM
- Boas práticas:
  - Nome da máquina: coisa-semana-nºmáquina
  - exemplo: web-sem2-m01
  - sempre que colocar mais de uma máquina em uma região, colocar em zonas diferentes
  - Máquinas E2 oferecem mais disponibilidade a baixo custo, amplamente utilizada no dia a dia.
  - Dentro dos SO’s o mais recomendado é o Debian, que prioriza a segurança e estabilidade, caso seja um sistema já implementado, usar a versão Linux 10, se vou colocar um novo sistema, Linux 11 mais recente.

Após a máquina criada, faremos a atualização do SO com o comando ***sudo apt update***

Comandos mais utilizados:

| Comando                        | Função                                                       |
| ------------------------------ | ------------------------------------------------------------ |
| sudo apt update                | Busca as atualizações disponíveis                            |
| sudo apt upgrade               | Pega o que tem de atualizável, baixa e instala               |
| apt install                    | Busca um novo apt e instala                                  |
| pwd                            | (Print Work Diretory) verifica onde você está no sistema     |
| ls                             | (List) lista o que tem no diretório                          |
| ls -l                          | Lista com detalhes                                           |
| mkdir                          | criar diretório                                              |
| cd /pasta cd .. cd /home/ cd ~ | navega pelos diretórios                                      |
| vim e nano                     | cria arquivo (no vim, para iniciar a digitação, pressiona i primeiro, esc para sair da edição, :w para salvar, :q para sair ou :q! para sair sem salvar as alterações ou :wq para salvar e sair) |
| rm e rmdir                     | remove pastas ou arquivos/ remove apenas pastas (rm - r remove tudo que tem dentro da pasta) |

<h3>Servidores Web</h3>

Definição e conceitos principais. A comunicação entre servidor x cliente é feito pelo protocolo HTTP.

- ***\**\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*Conceito de Alta Disponibilidade:\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\****

  O **Auto-Scaling**, é um serviço onde você determina o numero min e max de máquinas que vão prover o seu serviço e a partir desse dado a própria plataforma identifica a necessidade de aumentar ou diminuir a demanda operacional, garantindo alta disponibilidade com otimização dos gastos.

  O **Auto Healing**, promove a disponibilidade da aplicação, de tempos em tempos ele irá fazer uma verificação de disponibilidade da aplicação e no caso de haver algum problema que torne ela indisponível, ele mata a máquina e sobe outra com as características do modelo já predefinidos.

  Mantendo esses dois serviços disponíveis, garante que minha aplicação, pelo menos a nível de infraestrutura, ela esteja sempre estável e escalável. O trabalho de gerenciar esses serviços é do **Load Balance,** além de receber e balancear o fluxo de requisições à minha aplicação.

  Esse conceito de ter várias máquinas trabalhando em conjunto para atender um serviço específico é um exemplo de **clusterização,** que é o **instace group.**

  Agora iremos criar um modelo de servidor web de alta disponibilidade que use os conceitos falados nesse tópicos.

  - Criamos primeiro um modelo para que o Load Balance consiga deixar a máquina disponível para subir de forma automatizada.

    - Na opção de script de inicialização você define o que você precisa que o sistema execute assim que criar uma nova máquina.

      exemplo de script:

      ```
      #! **/bin/bash
       apt update
       apt -y install apache2
       cat <<EOF > /var/www/html/index.html
       <html><body><p>Olá, essa é minha página web!</p></body></html>**
      ```

Com o template nós podemos criar uma nova instancia ou um grupo de instancia, somente precisamos setar a região e zona.

Após criar a grupo de instancias, nós criamos o **health check** para fazer a verificação de integridade da minha aplicação e no caso da verificação falhar x vezes (numero que cadastrarmos como consecutive failures) aí ela mata a máquina e cria uma nova no lugar (**Auto Healing**).

Para verificar o altoScalling: instalar o htop (sudo apt htop), a gente precisa colocar o uso da CPU acima do programado e subir uma terceira máquina.

comando: **cat /dev/zero > /dev/null** a máquina vai entrar em um loop infinito, que vai fazer ela trabalhar em 100%.

### Load Balance:

Após deixar a aplicação do servidor web com alta disponibilidade, precisamos configurar o load balance para que ele realize a gerência dos acessos a nossa aplicação.

Nele, nós fazemos a configuração de **front-end**, para basicamente criar a porta e o ip que ficará disponível para aplicação do DNS e utilização do usuário e o back-end, para realizar de fato o balanceamento entre as requisições e máquinas, bem como definir parâmetros de utilização máxima.