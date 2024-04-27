# n8n_whatsapp_youtube_tuotrial
https://youtu.be/tulPqjhwm_M

# n8n-install-portainer
## Create a Docker volume for Portainer
```bash
sudo apt update && sudo apt upgrade
sudo apt install certbot python3-certbot-nginx
apt  install docker.io
docker volume create portainer_data
```

## Run the Portainer container
```bash
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```
then go to
https://ip:9443

create volume in portainer:
```bash
n8n_data
traefik_data
```

then create new stack in portainer:
then copy the following 

```bash
https://docs.n8n.io/hosting/installation/server-setups/docker-compose/#5-create-docker-compose-file
 ```
create Environment variables
 
then copy the following
https://docs.n8n.io/hosting/installation/server-setups/docker-compose/#6-create-env-file
 

```bash
DOMAIN_NAME=domain.net

SUBDOMAIN=n8n

GENERIC_TIMEZONE=Europe/Berlin
 
SSL_EMAIL=ibrahim@domain.net
 ```
