# Onderzoek naar DNS (Domain Name System)

## Inhoudstafel

1. [Waar staat DNS voor?](#1-waar-staat-dns-voor)
2. [Definitie en uitleg](#2-definitie-en-uitleg)
3. [Hoe draagt DNS bij aan het internet?](#3-hoe-draagt-dns-bij-aan-het-internet)
4. [Veiligheid](#4-veiligheid)
5. [DNS-vertragingen](#5-dns-vertragingen)
6. [DNS-spoofing](#6-dns-spoofing)
7. [Samenvatting](#7-samenvatting)
8. [Bronnen](#8-bronnen)

---

## 1. Waar staat DNS voor?

DNS staat voor **Domain Name System**. Het is een systeem dat domeinnamen omzet naar IP-adressen.

## 2. Definitie en uitleg

DNS kun je zien als een soort **telefoonboek van het internet**. Wanneer je bijvoorbeeld een website wilt bezoeken, typ je een domeinnaam in, zoals `google.com`. DNS zoekt hierbij het IP-adres van de website op.

Computers communiceren namelijk met IP-adressen. Dankzij DNS hoeven gebruikers deze IP-adressen niet zelf te onthouden.

## 3. Hoe draagt DNS bij aan het internet?

DNS maakt het internet gebruiksvriendelijker. Het zorgt ervoor dat mensen websites kunnen bezoeken door eenvoudig een domeinnaam in te typen.

Zonder DNS zouden gebruikers het IP-adres van iedere website moeten kennen. DNS zorgt er dus voor dat domeinnamen gekoppeld worden aan de juiste servers.

## 4. Veiligheid

DNS helpt bij het vinden van de juiste server, maar DNS zelf zorgt niet automatisch voor een volledig veilige verbinding. Er bestaan daarom technieken zoals **DNS over HTTPS (DoH)** en **DNS over TLS (DoT)** die DNS-aanvragen kunnen versleutelen.

Als een hacker DNS-verkeer kan manipuleren, kan een gebruiker bijvoorbeeld naar een verkeerde website worden doorgestuurd. Hierdoor kunnen gegevens zoals gebruikersnamen, wachtwoorden of andere persoonlijke gegevens mogelijk worden gestolen.

## 5. DNS-vertragingen

Een DNS-vertraging betekent dat het langer duurt om een domeinnaam naar het juiste IP-adres te vertalen.

Dit kan ervoor zorgen dat een website **langzamer begint te laden**. Bij meerdere DNS-aanvragen kunnen deze vertragingen zich opstapelen. DNS-caching kan helpen om dit probleem te verminderen doordat eerder opgezochte adressen tijdelijk worden opgeslagen.

## 6. DNS-spoofing

DNS-spoofing is een aanval waarbij iemand probeert valse DNS-informatie te geven. Hierdoor kan een gebruiker naar een verkeerd IP-adres worden gestuurd.

Een aanvaller kan bijvoorbeeld proberen een gebruiker naar een nagemaakte website te sturen. Als de gebruiker daar gegevens invult, kunnen deze gegevens in handen van de aanvaller komen.

## 7. Samenvatting

DNS staat voor **Domain Name System** en zorgt ervoor dat domeinnamen worden gekoppeld aan IP-adressen. Hierdoor is het internet gemakkelijker te gebruiken.

DNS kan ook te maken krijgen met veiligheidsproblemen. DNS-vertragingen kunnen websites langzamer laten laden en bij DNS-spoofing kan een gebruiker naar een verkeerde website worden doorgestuurd.

## 8. Bronnen

* Oracle. (z.d.). *What is big data?*
* Cloudflare. (z.d.). *What is DNS?*
* Mozilla. (z.d.). *DNS over HTTPS*
