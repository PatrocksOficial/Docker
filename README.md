# Docker

O que é Docker?

Docker é um software que reduz a complexidade de setup de aplicações (não precisar baixar várias coisas como mysql, php, sql, .net version e etc).
Onde configuramos os containers são como os servidores para rodar nossas aplicações.
Com facilidade, pode-se criar ambientes totalmente independentes e que funcionam em diversos SO's.
Torna os projetos performáticos.


Por que utilizá-lo?

O Docker proporciona mais velocidade na configuração de ambiente, seja um deploy, servidor de ambientação, ambiente de testes e afins.
Pouco tempo gasto em manutenção, containers são executados como configurados.
Performance para executar aplicação, mais performático que uma Máquina Virtual.
Nos livra de Matrix from Hell.


O que é Matrix from Hell?

Aplicações complexas e diferentes para rodar na mesma empresa, o que ocorre, ter que configurar várias coisas para rodar somente em um pc, nesse caso como seria com docker e images, basta configurar e acabou, uma vez configurado é fácil de replicar em diversos outros computadores e dar manutenção.


Diferença de versões em docker?

O Docker é dividido em duas versões: CE x EE
CE é a Community Edition, edição gratuita, que nos possibilita utilizar o Docker normalmente.
EE é a Enterprise Edition, edição paga, há uma garantia maior das versões que são disponibilizadas e você tem suporte do time do Docker caso precise.

Como rodar um container:
![image](https://github.com/PatrocksOficial/Docker/assets/87246660/ec9a1bfe-a5a7-46ab-ba65-6e96422f4bb3)

O que são containers?

São um pacote de códigos que podem executar uma ação, por exemplo, rodar uma aplicação de Node.js, PHP, Python e etc.
Ou seja, nossos projetos seram utilizados dentro dos containers que criarmos/utilizarmos.
Containers geralmente são separados cada um para executar somente uma função, exemplo, um container para rodar o banco em mysql, um container para rodar a aplicação em C# e dentre outros.
Containers utilizam as imagens para serem executados.
Você pode utilizar múltiplos containers para rodar juntos diversas aplicações como citei acima.


Container x Imagem

Imagem e Container são recursos fundamentais do Docker.
Imagem é o próprio "projeto" que será executado pelo container, todas as instruções estarão declaradas nela.
Container é o Docker rodando alguma imagem, consequentemente executando algum código proposto por ela.

O fluxo é: Programar uma imagem e executá-la por meio de um container.


Onde encontrar imagens?

Vamos encontrar imagens no repositório do Docker: https://hub.docker.com
No site pode verificar quais as imagens existem das linguagens e tecnologias que estamos procurando, exemplo C#, Java, Node.js.
E também aprender como utilizá-las.
Executar a imagem em um container com docker run <imagem>
docker run -it <imagem, ex, ubuntu>


Como verificar containers executados?

O comando docker ps ou docker container ls exibe quais containers estão sendo executados no momento, utilizando  a flag -a, temos também todos os containers já executados na máquina.
Este comando é útil para entender o que está sendo executado e o que acontece no ambiente.

Executando container com interação

É possível rodar um container e deixar ele executando no terminal, para fazer isso é necessário utilizar a flag -it.
Desta forma é possível executar comandos disponíveis nos containers que estamos utilizando, rodando o comando run.


Container x VM

Container é uma aplicação que serve para um determinado fim, não possuindo um sistema operacional que consome um tamanho gigantesco, o container pesa alguns mbs;
VM possui um sistema operacional próprio, tamanho de gbs, pode executar diversas funções ao mesmo tempo.
Containers acabam gastando menos recursos para serem executados por causa do seu uso específico.
VM gastam mais recursos porém exercem mais funções.


Rodando container em background

Quando iniciamos um container que persiste, ele fica ocupando o terminal, para resolver isso, pode-se executar um container em background, para não precisar ficar com diversas abas de terminal aberto, utiliza a flag -d(detached);
Verifica também os containers em background com docker ps.


Expor portas

Os containers de docker não tem conexão com nada de fora deles, por conta disso, precisa expor as portas, a flag é a -p e podemos fazer por exemplo assim: -p 80:80;
Desta forma o container vai estar acessível na porta 80.

exemplo: docker run -d -p 3000: 80
esses 3000 vai ser a porta que vai ser exposta para utilizar, então seria localhost:3000.
o 80 seria a porta que eu quero receber do docker.


Parando Containers

Podemos parar um container com o comando docker stop <id ou nome>, desta maneira estamos liberando recursos.
Pode verificar os containers que estão rodando com o comando docker ps.


Iniciando um container

Para voltar a rodar um container pode rodar o comando docker start <id>, sempre que for utilizar o comando docker run ele vai criar um novo container, então caso for aproveitar um antigo, utilize o start.


Definindo nome do container

Pode definir um nome do container com  a flag --name.
Se não colocar um nome, será gerado aleatoriamente, o que pode ser um possível problema em um ambiente profissional.
A flag run é inserida junto do comando run.


Verificando os logs

Podemos verificar o que acontece com um container usando o seguinte comando: Docker logs <id>
Quaisquer alteração será exibida no log.


Removendo containers

Para remover um container da máquina que estamos executando, pode utilizar o seguinte comando: docker rm <id>.
Caso o container estiver rodando, pode utilizar a flag -f(force).
O container removido não é mais listado no docker ps -a
