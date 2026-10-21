# Onderzoek: DNS (Domain Name System)

## Inhoudstafel

- [1. Waar staat DNS voor?](#1-waar-staat-dns-voor)
- [2. Definitie en uitleg](#2-definitie-en-uitleg)
- [3. Hoe draagt DNS bij aan het internet?](#3-hoe-draagt-dns-bij-aan-het-internet)
- [4. Veiligheid](#4-veiligheid)
- [5. DNS-vertragingen](#5-dns-vertragingen)
- [6. DNS-spoofing](#6-dns-spoofing)
- [7. Samenvatting](#7-samenvatting)
- [8. Bronnen](#8-bronnen)

## 1. Waar staat DNS voor?

DNS staat voor **Domain Name System**. Het is een systeem dat domeinnamen, zoals `www.google.com`, koppelt aan IP-adressen. Een computer heeft een IP-adres nodig om een server op het internet te kunnen vinden. DNS zorgt ervoor dat de gebruiker niet telkens zelf een moeilijk IP-adres hoeft te onthouden.

## 2. Definitie en uitleg

DNS kan je vergelijken met een **telefoonboek van het internet**. In plaats van een telefoonnummer op te zoeken, zoekt je computer via DNS het IP-adres dat bij een domeinnaam hoort.

Wanneer je bijvoorbeeld een website intypt, vraagt je computer aan een DNS-resolver welk IP-adres bij die website hoort. De resolver kan het antwoord uit zijn cache halen. Als het antwoord daar niet aanwezig is, kan hij andere DNS-servers raadplegen totdat het juiste antwoord gevonden is. Daarna kan je computer verbinding maken met de webserver.

DNS werkt met verschillende soorten records. Een **A-record** kan bijvoorbeeld een domeinnaam aan een IPv4-adres koppelen. Een **CNAME-record** kan een alias naar een andere domeinnaam verwijzen. DNS gebruikt ook andere records voor bijvoorbeeld mailservers en naamservers.

![Schema van een DNS-zoekopdracht](dns-schema.png)

*Figuur 1: Vereenvoudigd schema van een DNS-zoekopdracht.*

## 3. Hoe draagt DNS bij aan het internet?

DNS is een belangrijk onderdeel van de werking van het internet. Zonder DNS zouden gebruikers veel vaker IP-adressen moeten kennen om websites en andere online diensten te bereiken.

Een belangrijk voordeel is dat DNS domeinnamen leesbaar maakt voor mensen. Een naam zoals `www.voorbeeld.be` is veel gemakkelijker te onthouden dan een IP-adres.

DNS helpt ook bij de prestaties. DNS-servers kunnen antwoorden tijdelijk **cachen**. Daardoor hoeft niet iedere aanvraag helemaal opnieuw te worden opgezocht. Volgens Google kunnen complexe webpagina's meerdere DNS-opzoekingen nodig hebben voordat ze beginnen te laden. Caching kan het aantal nieuwe opzoekingen verminderen. (Google, 2024)

De werking van DNS kan eenvoudig worden samengevat:

| Stap | Wat gebeurt er? |
|---|---|
| 1 | De gebruiker typt een domeinnaam in. |
| 2 | De computer vraagt het bijbehorende IP-adres op. |
| 3 | De DNS-resolver controleert zijn cache. |
| 4 | Indien nodig worden andere DNS-servers geraadpleegd. |
| 5 | Het IP-adres wordt teruggegeven. |
| 6 | De browser maakt verbinding met de webserver. |

## 4. Veiligheid

DNS is belangrijk voor de bereikbaarheid van websites, maar het oorspronkelijke DNS-protocol is niet ontworpen als een volledig beveiligd communicatiekanaal. Daarom bestaan er extra beveiligingsmaatregelen.

Een voorbeeld is **DNSSEC** (Domain Name System Security Extensions). DNSSEC helpt controleren of een DNS-antwoord authentiek is en onderweg niet op een ongewenste manier is aangepast. Daarnaast bestaan er versleutelde manieren om DNS-verzoeken te versturen, zoals **DNS over HTTPS (DoH)** en **DNS over TLS (DoT)**. Deze kunnen helpen voorkomen dat DNS-verzoeken onderweg eenvoudig worden afgeluisterd of aangepast. (Google, 2024)

### Welke gegevens kunnen worden gestolen?

DNS bevat normaal gesproken vooral informatie over domeinnamen en netwerkadressen. Als een aanvaller toegang krijgt tot DNS-verkeer of DNS-infrastructuur, kan die bijvoorbeeld informatie krijgen over welke domeinen een apparaat probeert te bereiken. Dat kan informatie geven over het online gedrag van een gebruiker of organisatie.

Het is belangrijk om te weten dat DNS zelf normaal gesproken niet de inhoud van bijvoorbeeld een wachtwoord of bericht bevat. Die gegevens worden meestal via andere protocollen verstuurd. Wanneer een aanvaller DNS manipuleert, kan het gevaar vooral ontstaan doordat een gebruiker naar een verkeerde server wordt gestuurd.

## 5. DNS-vertragingen

DNS-vertraging betekent dat het langer duurt voordat een domeinnaam naar een IP-adres wordt vertaald. Hierdoor kan het lijken alsof een website langzaam begint te laden.

Een DNS-vertraging kan ontstaan door bijvoorbeeld:

- een grote afstand tussen de gebruiker en de DNS-server;
- een overbelaste DNS-server;
- netwerkproblemen;
- een DNS-cache die het benodigde antwoord niet bevat;
- problemen of aanvallen die veel verkeer veroorzaken.

Google beschrijft dat een cache-miss ervoor kan zorgen dat een DNS-resolver meerdere andere DNS-servers moet raadplegen. Dat kan extra netwerkvertraging veroorzaken. (Google, 2024)

DNS-vertraging is vooral merkbaar wanneer een webpagina veel verschillende domeinen gebruikt. Voor ieder nieuw domein kan namelijk een DNS-opzoeking nodig zijn.

## 6. DNS-spoofing

**DNS-spoofing** is een aanval waarbij een aanvaller probeert een gebruiker een verkeerd DNS-antwoord te laten ontvangen. In plaats van het echte IP-adres kan bijvoorbeeld het IP-adres van een andere server worden teruggegeven.

Een eenvoudig voorbeeld:

1. Een gebruiker wil naar `www.voorbeeld.be`.
2. De computer vraagt via DNS het IP-adres op.
3. Een aanvaller zorgt ervoor dat een verkeerd DNS-antwoord wordt gebruikt.
4. De gebruiker wordt naar een andere server gestuurd.
5. Die server kan bijvoorbeeld een nagemaakte website tonen.

Dit kan gevaarlijk zijn omdat een gebruiker kan denken dat hij op de echte website zit terwijl hij naar een verkeerde server is gestuurd. DNSSEC en beveiligde DNS-transporten kunnen helpen om dit soort risico's te verminderen. (Google, 2024)

DNS-spoofing kan dus gevolgen hebben voor de **vertrouwelijkheid**, **integriteit** en **veiligheid** van online communicatie. Een aanvaller kan bijvoorbeeld proberen gebruikers om te leiden naar een phishingwebsite.

## 7. Samenvatting

DNS staat voor **Domain Name System** en zorgt ervoor dat domeinnamen worden gekoppeld aan IP-adressen. Hierdoor kunnen mensen websites gebruiken met gemakkelijk te onthouden namen in plaats van IP-adressen.

DNS is belangrijk voor de functionaliteit van het internet omdat browsers en andere programma's hierdoor servers kunnen vinden. Caching kan ervoor zorgen dat DNS-opzoekingen sneller verlopen.

DNS heeft ook een veiligheidskant. Aanvallen zoals DNS-spoofing kunnen gebruikers naar verkeerde servers sturen. Beveiligingstechnieken zoals DNSSEC, DNS over HTTPS en DNS over TLS kunnen helpen om DNS veiliger te maken.

**Kort gezegd:** DNS is een soort adresboek van het internet. Het vertaalt namen die mensen gebruiken naar adressen die computers nodig hebben.

## 8. Bronnen

Google. (2024). *Introduction to Google Public DNS*. Google for Developers. https://developers.google.com/speed/public-dns/docs/intro

Google. (2024). *Performance benefits*. Google for Developers. https://developers.google.com/speed/public-dns/docs/performance

Google. (2024). *Security benefits*. Google for Developers. https://developers.google.com/speed/public-dns/docs/security

Mockapetris, P. (1987). *Domain names—Implementation and specification (RFC 1035)*. RFC Editor. https://www.rfc-editor.org/rfc/rfc1035

