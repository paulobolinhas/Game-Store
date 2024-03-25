# Projeto
# Projeto de PSI 2022/23

# Objetivo do projeto
A vossa empresa decidiu melhorar a divulgação dos jogos produzidos, implementando um sistema que proporciona mais visibilidade de seus produtos e permite uma maior interação entre os seus jogadores. A vossa equipa de desenvolvimento foi incubida de iniciar o desenvolvimento deste projeto fundamental para o futuro da empresa!

# Execução do projeto
As características deste projeto requerem uma equipa composta por 5 elementos, com competências e responsabilidades bem definidas e distintas, que serão avaliadas. Devido à importância do projeto, o processo de avaliação seguirá regras rigorosas. A constituição das equipas é realizada na atividade Grupos de PSI na página de PSI no Moodle. O projeto seguirá uma metodologia de desenvolvimento de software inspirada na metodologia Kanban, que possui papéis e atividades bem definidos, operacionalizada pela plataforma JIRA Agile.

Como parte da metodologia Kanban, o conjunto de funcionalidades a implementar durante cada sprint é definido no início do sprint. O backlog inicial é composto pelos itens abaixo (estes itens podem sofrer alterações a qualquer momento). Todos estes itens têm os seguintes critérios de aceitação em comum: (i) deve ser possível concluir o processo num browser desktop ou mobile; (ii) deve ser possível concluir o processo num browser desktop sem usar o rato.

Em cada sprint pretende-se que seja construída uma versão completa de funcionalidades do sistema de informação na framework escolhida. No final de cada sprint é feita uma demonstração das funcionalidades.

# Restrições 
Quaisquer imagens e vídeos ilustrativos devem estar alojados externamente.

# Aspetos técnicos
Os projetos utilizarão servidores implementando o stack tecnológico MEAN (MongoDB, Express, Angular, NodeJS). Os clientes terão obrigatoriamente de ser browsers web. É ainda necessário estruturar o sistema de informação de acordo com as seguintes quatro camadas: 1) cliente browser; 2) servidor web com lógica de apresentação; 3) servidor aplicacional com regras de negócio; e 4) servidor de base de dados.

# Plataforma de execução do projeto
O projeto deve ser executado no servidor appserver.alunos.di.fc.ul.pt

O acesso ao servidor é feito através de ssh sendo o username o número do grupo. A password inicial é também o número do grupo e deve ser alterada após o primeiro login

> ssh psi050@appserver.alunos.di.fc.ul.pt
O appserver tem instalados node, npm e mongo. Todos os módulos necessários para funcionamento do projeto devem ser instalados recorrendo ao npm.

Cada grupo tem uma base de dados criada no servidor mongo. O nome da base de dados é igual ao número do grupo (p.ex. o grupo psi050 deve usar a base de dados psi050). 

Cada grupo tem um utilizador no servidor mongo. O nome do utilizador é igual ao número do grupo. A password também é igual ao número do grupo. Para acederem à consola do mongo usem o comando (substituindo psiXXX pelo número do grupo)

mongo --username psiXXX --password --authenticationDatabase psiXXX appserver.alunos.di.fc.ul.pt/psiXXX
Cada grupo tem dois portos abertos para acesso por http a servidores node. O primeiro porto no intervalo 3001 a 3035 e o segundo porto no intervalo 3051 a 3085. Por exemplo, o grupo psi003 deve usar os portos 3003 e 3053. É assim importante que configurem os servidores node (para o front-end e back-end) nesses portos.

A forma de executar o servidor node que serve o front-end Angular deve ser a seguinte (onde o XXXX que define o porto deve ser o específico de cada grupo)

ng serve --port XXXX --host 0.0.0.0 --disableHostCheck true
Para o servidor node que serve o back-end não é necessário mudar a forma de execução.

A connection string para acesso à base de dados mongo deve ser a seguinte (onde devem substituir psiXXX pelo número do grupo)

mongodb://psiXXX:psiXXX@localhost:27017/psiXXX?retryWrites=true&authSource=psiXXX
Recomendação sobre o processo de desenvolvimento (controlo de versões)
É vivamente recomendado que utilizem a plataforma git (git.alunos.di.fc.ul.pt) durante o desenvolvimento do projeto. O uso de controlo de versões irá facilitar o trabalho de uma equipa de 5 pessoas e irá permitir passar o código desenvolvido nas máquinas de desenvolvimento para o servidor de demonstração de uma forma fácil.

Recomenda-se vivamente que criem um branch no repositório para cada tarefa que seja criada na ferramenta JIRA. O branch deve ser identificado pelo número da tarefa no JIRA de modo a permitir a sua identificação de uma forma quase imediata.
