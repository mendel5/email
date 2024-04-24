# email
Information about how to configure email servers, services, etc.

Note: Some content is focused on Germany.

## Verbindungen
- E-Mail-Client <--> E-Mail-Server
- E-Mail-Server <--> E-Mail-Server <-- in diesem Repository geht es hauptsächlich um diese Art von Verbindungen.

## Wichtige Funktionen
- SPF
  - Sender Policy Framework
  - https://en.wikipedia.org/wiki/Sender_Policy_Framework
  - SPF is an email validation protocol designed to detect and block email spoofing by verifying sender IP addresses against the email domain's authorized senders list published in DNS records.
- DKIM
  - DomainKeys Identified Mail
  - https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail
  - DKIM is an email authentication method that allows the receiver to check that an email claimed to have come from a specific domain was indeed authorized by the owner of that domain through cryptographic signatures.
- DMARC
  - Domain-based Message Authentication, Reporting and Conformance
  - https://en.wikipedia.org/wiki/DMARC
  - DMARC is an email authentication, policy, and reporting protocol that builds on SPF and DKIM to enhance the domain owners' ability to prevent their domains from being used for email spoofing, phishing scams, and other cybercrimes.
- DNSSEC
  - Domain Name System Security Extensions
  - https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions
  - DNSSEC is a set of protocols that add a layer of security to the DNS lookup and response process by digitally signing data to validate its authenticity, thus protecting against DNS spoofing.
- DANE
  - DNS-based Authentication of Named Entities
  - https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities
  - DANE is a protocol used to secure internet connections by allowing DNS records to specify what certificates are trustworthy for a given domain, preventing attacks on the TLS (Transport Layer Security) protocol.
  - DANE can only be used effectively if DNSSEC is enabled.
- MTA-STS
  - Message Transfer Agent, Strict Transport Security
  - https://en.wikipedia.org/wiki/MTA-STS
  - MTA-STS is a security standard used to enforce transport layer (TLS) encryption and authenticate email in transit between servers, preventing interception and tampering by mandating HTTPS for SMTP connections.
  - With MTA-STS a TLS encryption is enforced while with StartTLS a TLS encryption is optional.

## Testing
### Testing Allgemein
- https://mecsa.jrc.ec.europa.eu/en/ EU Email Communications Security Assessment (MECSA)
- https://mxtoolbox.com/supertool
- https://mxtoolbox.com/dmarc/dmarc-email-tools SPF DKIM DMARC
- https://dmarcly.com/tools/ SPF DKIM DMARC
- https://www.mail-tester.com/
- https://www.emailchecky.com/en/
- https://ssl-tools.net/
- https://www.checktls.com/index.html
- https://www.debouncer.com/reverse-dns-check
- https://testconnectivity.microsoft.com/tests/exo
- https://testconnectivity.microsoft.com/tests/O365DaneValidation/input
- https://dnschecker.org/all-tools.php
- https://toolbox.googleapps.com/apps/main/
- https://toolbox.googleapps.com/apps/dig/

### Testing DNSSEC
- https://dnssec-debugger.verisignlabs.com/
- https://www.experte.de/dns-check/dnssec
- https://dane.sys4.de/
- https://dnsviz.net/

## DNSSEC New
- https://joscor.com/blog/dane-tlsa-tutorial/
- https://www.msxfaq.de/signcrypt/dane_tlsa.htm
- https://thomas-leister.de/dane-tlsa-records-erklaert/
- https://ssl-tools.net/tlsa-generator
- https://github.com/internetstandards/toolbox-wiki/blob/main/DANE-for-SMTP-how-to.md
- https://github.com/internetstandards/toolbox-wiki
- https://internet.nl/
- https://www.dotplex.com/de/faq/dnssec-dane-tlsa
- https://www.infoblox.com/dns-security-resource-center/dns-security-faq/what-is-dane/

## Wissen
- https://support.google.com/a/answer/81126 Email sender guidelines
- https://www.nospamproxy.de/wp-content/uploads/Praxisleitfaden-DKIM-SPF-DMARC-DANE-1.pdf
- https://www.internetsociety.org/deploy360/dnssec/statistics/
- https://stats.labs.apnic.net/dnssec/
- https://stats.labs.apnic.net/dnssec
- https://blog.lindenberg.one/EmailSicherheitsTest
- https://www.heise.de/news/Transportsicherheit-BSI-zertifiziert-E-Mail-Dienste-nach-neuer-Richtlinie-9349117.html
- https://certified-senders.org/wp-content/uploads/2020/02/E-Mail-Transportverschluesselung-STARTTLS-vs.-DANE-vs.-MTA-STS_updated.pdf
- https://www.golem.de/news/smtp-mta-sts-bringt-sichere-verschluesselung-zwischen-mailservern-1809-136853.html
- https://beta-its.de/ultimative-domain-sicherheit-dnssec-mta-sts-dane-dmarc
- https://www.hornetsecurity.com/de/services/email-authentifizierung/
- https://www.anubisnetworks.com/blog/dmarc_dane_explained
- https://www.heise.de/news/iX-Workshops-Sichere-Datenuebertragung-mit-TLS-DNSSEC-und-DANE-6332452.html
- https://www.nslookup.io/learning/what-is-a-good-ttl-for-dns/ TTL
- https://www.varonis.com/blog/dns-ttl TTL
- https://support.google.com/a/answer/10032473 Tutorial for recommended DMARC rollout
- http://newweb.zytrax.com/books/dns/ch9/dmarc.html `_dmarc` / `_dmarc.example.com`
- https://support.google.com/a/answer/2466563 Add your DMARC record
- https://access.redhat.com/documentation/de-de/red_hat_enterprise_linux/4/html/reference_guide/s2-bind-zone-examples

## Hoster
### Allgemein
- https://www.hosttest.de/artikel/groesste-webhostinganbieter-in-deutschland
- https://www.trending.de/hosting/die-10-groessten-deutschen-hoster-und-meine-empfehlung/

### Microsoft
- https://www.windowspro.de/news/microsoft-unterstuetzt-dane-dnssec-exchange-online/04980.html
- https://learn.microsoft.com/de-de/purview/how-smtp-dane-works
- https://practical365.com/exchange-online-dnssec-dane/
- https://learn.microsoft.com/de-de/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider?view=o365-worldwide
- https://learn.microsoft.com/de-de/microsoft-365/enterprise/external-domain-name-system-records?view=o365-worldwide

### Hoster: IONOS
- https://www.ionos.de/hilfe/domains/domain-guard/dnssec-einrichten-und-verwalten/

### Hoster: Strato
- https://www.strato.de/faq/domains/wie-kann-ich-bei-strato-meine-dns-eintraege-verwalten/ (`smtpin.rzone.de`)
- https://www.strato.de/faq/domains/sichern-sie-ihre-webseite-mit-dnssec/
- https://www.strato.de/faq/domains/was-ist-domain-guard/
- https://www.strato.de/faq/hosting/DMARC-Policy/
- https://www.strato.de/faq/hosting/dmarc-bei-strato-aktivieren/
- https://www.strato.de/faq/mail/wie-kann-ich-fuer-meine-domain-die-dkim-einstellungen-aendern/
- https://www.strato.de/faq/mail/so-lauten-die-strato-e-mail-server/
- https://www.strato.de/faq/mail/externes-e-mail-programm-mit-strato-e-mail-adresse-nutzen/

### Hoster: Hetzner
- https://docs.hetzner.com/de/dns-console/dns/general/dns-overview/
- https://docs.hetzner.com/de/dns-console/dns/general/dnssec/
- https://docs.hetzner.com/dns-console/dns/general/dnssec/

## DNSSEC
Welche Hoster, Internetdienstanbieter, etc. unterstützen DNSSEC und welche nicht?

### DNSSEC wird unterstützt
- IONOS (1&1)
- Strato
- Microsoft Outlook 365

### DNSSEC wird nicht unterstützt
- Hetzner

### Prüfen
- OVH
- DigitalOcean
- Namecheap
- AWS
- GoDaddy
- Bluehost
- Siteground
- Contabo
- All-inkl / All inkl
- Domainfactory
- Host Europe
- Mittwald
- Netcup
- Alfahosting
- PlusServer
- ProfiHost
- WebGo
- 1Blu
- Dogado
- Goneo
- Checkdomain
