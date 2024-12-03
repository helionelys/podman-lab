# podman-lab
Laboratório de testes para manipulação de imagem container PostgreSQL usando o Podman, fazendo pull do Docker HUB e posterior push para Quay.io

## Recursos utilizados
- Máquina virtual tendo como sistema operacional base Fedora Workstation (41)
- Instalação do Podman

## Passos utilizados
#### - Download da imagem PostgreSQL:Latest do Docker HUB
##### $ podman pull docker.io/postgres:latest

#### - Listar imagem no repositório local
##### $ podman images

#### - Aplicando tag a imagem baixada
##### $ podman tag docker.io/library/postgres:latest postgres-hub4it:17

#### - Autenticação e envio da imagem do container para repositório do Quay.io
##### $ podma login quay.io 
##### username: helionelys
##### Password: **********

##### $ podman push postgres-hub4it:17 quay.io/heionelys/postgres-hub4it:17
