# Docker Taboo

To deploy Taboo using docker

0. Install docker: https://docs.docker.com/engine/installation/
0. Install docker-compose: https://docs.docker.com/compose/install/
0. Clone this repository and enter in the directory
  0. Duplicate tmpl_docker-compose.yml as docker-compose.yml and fix values accord your project
0. Clone taboo repository inside
  0. Fix app/Config accord your project
0. `$ docker-compose up -d`