# awsbootcamp
Anotações e Projetos Bootcamp DIO.me entregas

AWS = Amazon Web Services

Amazon fornece vários serviços em nuvem, indo desde rodar uma aplicação diretamente da AWS até rodar um servidor propriamente dito, em caráter virtual, com a oferta de algumas plataformas de sistema operacional.

Podendo substituir datacenter's parcialmente ou inteiros, interligando os equipamentos através de regras de rede.

Os serviços são ofertados por Região, podendo existir diferenças de valor da oferta de serviço entre si.

Para o publico em geral, ao contratar o serviço da AWS não se sabe exatamente o endereço dos datacenter da AWS, apenas as cidades que fazem parte daquela "Region"


EC2 - Elastic Computer Cloud é uma maquina virtual mesmo, com cpu, HD, RAM, (virtualizados)
    - Existem várias categorias, por tipo de uso e também, por disponibilidade na Region
    - Categorias para maior armazenamento, para maior performance, etc, para determinados tipos de aplicação, utilizados siglas que podem ser entendidas na vasta documentação da propria amazon

S3 (Simple Storage Service)- Tipos de armazenamento, o que me chamou atenção éa forma de armazenamento S3 Glacier que funciona como um arquivão geral e guardado "como em armarios" onde são armazenados automaticamente dados muito pouco ou quase nada utilizados.

EBS (Elastic Block Store)- Como se "um hd externo" espetado em um equipamento, pode funcionar com snapshot's (cópias de sombra), deve ser utilizado mais para armazenamento de arquivos de sistemas que serão realmente utilizados, para todo o resto é recomendado o S3, os snapshots podem ser feitos e também devem ser armazenados em um S3. Aplicações podem ser apontadas diretamente para ele, e processada por um EC2.

Basicamente, sobre tudo que vi agora o funcionamento é como IaaS (Infraestructure as a Service), ou seja, a AWS fornece toda a infraestrutura, mas a forma que eu utilizo a infraestrutura, desde segurnaça de dados (além de uma camada pré-existente da Amazon) mas toda a cofiguração de aplicação que eu armazenar, configurar, e inserir para proteger ou não é por minha conta, pela AWS estou contratando apenas a IaaS, todo o resto eé responsabilidade minha.

Com IAM é possível gerar usuários (logins) e suas permissões através de políticas tanto de senha quanto de função. É possível habilitar MFA para cada conta.

Inicialmente a primeira conta é root, recomenda-se como boa prática que se crie uma senha muito forte para esta conta, por ser a controladora de tudo, contas, politicas, permissões, funções, custos, tudo, e crie-se outra que mesmo que tenha as mesmas permissões de "administrador geral" das suas contas dentro da AWS, se acontecer algo com esta outra conta, ainda se tem a root para desfazê-la, criar outras contas, retomar o controle, e recomeçar, ou utilizar em um disaster recovery.

É possível fazer espelhamento entre aplicações em diferentes Regions.

E muito mais, assim como os equipamentos EC2 é possível subir serviços apenas de banco de dados, apenas de aplicações, apenas de interligação entre um sistema e outro.


Toda aplicação gera um custo, então com a conta root é possível acessar também uma parte de billing, e alarmes quando atingir um certo valor.

É possivel tambpem programar liga/desliga da aplicação, regras de escalonamento, tempo e horários de utilização, etc.
