# Docker-Compose-Zabbix
 
Este repositorio tem como objetivo forncer uma maneira facil e simples de executar um Zabbix Server utilizando Docker.

## Instalando dependencias:

### Instalando docker
```shell
curl -fsSL https://get.docker.com | sh
```
### Instalando o docker-compose
```shell
curl -L https://github.com/docker/compose/releases/download/1.25.5/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
````
```shell
chmod +x /usr/local/bin/docker-compose
```
### Descarregando o repositorio do projeto
```shell
cd /opt/
git clone https://github.com/n4bs/Zabbix-Docker-Compose.git Zabbix
cd Zabbix
```

### Criando persistencia para os dados
```bash
mkdir -p ./zbx_env/usr/lib/zabbix/externalscripts \
./zbx_env/etc/zabbix/zabbix_agentd.d \
./zbx_env/var/lib/zabbix/modules \
./zbx_env/var/lib/zabbix/enc \
./zbx_env/var/lib/zabbix/snmptraps \
./zbx_env/var/lib/mysql
```
### Iniciando o Zabbix com Docker compose
```shell
docker-compose up -d
```

### Aceder ao zabbix
Para aceder ao zabbix utilize 

http://ip_do_seu_servidor:80

Utilizdor: Admin
Password: zabbix