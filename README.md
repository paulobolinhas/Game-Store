# Project
# PSI Project 2022/23

# Project's goal
Your company decided to improve the dissemination of the games produced, implementing a system that provides more visibility for your products and allows greater interaction between your players. Your development team was tasked with starting the development of this fundamental project for the future of the company!

# Project execution
The characteristics of this project require a team made up of 5 members, with well-defined and distinct skills and responsibilities, which will be evaluated. Due to the importance of the project, the evaluation process will follow strict rules. The formation of teams is carried out in the PSI Groups activity on the PSI page in Moodle. The project will follow a software development methodology inspired by the Kanban methodology, which has well-defined roles and activities, operated by the JIRA Agile platform.

As part of the Kanban methodology, the set of features to be implemented during each sprint is defined at the beginning of the sprint. The initial backlog consists of the items below (these items may change at any time). All of these items have the following acceptance criteria in common: (i) it must be possible to complete the process on a desktop or mobile browser; (ii) it must be possible to complete the process in a desktop browser without using the mouse.

In each sprint, the aim is to build a complete version of the information system's functionalities in the chosen framework. At the end of each sprint, a demonstration of the features is made.

# Restrictions
Any illustrative images and videos must be hosted externally.

# Technical aspects
The projects will use servers implementing the MEAN technology stack (MongoDB, Express, Angular, NodeJS). Customers must be web browsers. It is also necessary to structure the information system according to the following four layers: 1) browser client; 2) web server with presentation logic; 3) application server with business rules; and 4) database server.

# Project execution platform
The project must be run on the appserver.vamos.di.fc.ul.pt server

Access to the server is done through ssh with the username being the group number. The initial password is also the group number and must be changed after the first login

> ssh psi050@appserver.alunos.di.fc.ul.pt
The appserver has node, npm and mongo installed. All modules necessary for the project to function must be installed using npm.

Each group has a database created on the mongo server. The database name is the same as the group number (e.g. group psi050 must use database psi050).

Each group has a user on the mongo server. The user name is the same as the group number. The password is also the same as the group number. To access the mongo console, use the command (replacing psiXXX with the group number)

mongo --username psiXXX --password --authenticationDatabase psiXXX appserver.alunos.di.fc.ul.pt/psiXXX
Each group has two ports open for http access to node servers. The first port in the range 3001 to 3035 and the second port in the range 3051 to 3085. For example, the psi003 group must use ports 3003 and 3053. It is therefore important that you configure the node servers (for the front-end and back-end ) in these ports.

The way to run the node server that serves the Angular front-end must be as follows (where the XXXX that defines the port must be specific to each group)

ng serve --port XXXX --host 0.0.0.0 --disableHostCheck true
For the node server that serves the back-end, it is not necessary to change the way of execution.

The connection string to access the mongo database must be the following (where psiXXX must be replaced by the group number)

mongodb://psiXXX:psiXXX@localhost:27017/psiXXX?retryWrites=true&authSource=psiXXX
Recommendation on the development process (version control)
It is strongly recommended that you use the git platform (git.vamos.di.fc.ul.pt) during project development. The use of version control will facilitate the work of a team of 5 people and will allow the code developed on the development machines to be transferred to the demo server in an easy way.

It is strongly recommended that you create a branch in the repository for each task that is created in the JIRA tool. The branch must be identified by the task number in JIRA in order to allow its identification almost immediately.
