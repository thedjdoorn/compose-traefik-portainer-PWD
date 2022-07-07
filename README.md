# Deployment van Portainer en Traefik op Play With Docker

## Over deze repository
Deze repository bevat alle bestanden om eenvoudig een Portainer/Traefik omgeving op te zetten op Play With Docker.

## Getting started
- Clone deze repository in je Play With Docker omgeving
- Kopieër `.env.example` naar `.env`
- Pas de `.env` aan met vim, zodat de `PWDOCKER_DOMAIN` variabele geset is naar het hoofddomein van je Play With Docker omgeving
- Maak het netwerk proxy aan met `docker network create proxy`
- Start Traefik en Portainer met `docker-compose up`
- Hierna zouden Traefik en Portainer bescikbaar moeten zijn op subdomeinen traefik.example.com en portainer.example.com. Op het Traefik dashboard kan worden ingelogd met user/changeme

## Traefik
Omdat PWD ook gebruikt kan worden zonder https gebruiken we in dit project geen LetsEncrypt certificaten, die vallen buiten de scope. De gebruikersnaam/wachtwoord combinatie voor het Traefik Dashboard is `user`/`changeme`.
