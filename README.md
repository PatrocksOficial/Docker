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

