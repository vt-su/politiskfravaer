# Politisk fravær
Politisk fravær-generator basert på [mpdf](http://mpdf.github.io)

## Forutsetninger
- Linux-server med [Apache](https://httpd.apache.org) installert ([Ubuntu](https://ubuntu.com)/Debian anbefales)
- PHP-versjon mellom 5.6.0 og 7.4.0 er påkrevd ([Se alle krav for mPDF](http://mpdf.github.io/about-mpdf/requirements-v7.html))
  - `mbstring`, `mbregex` og `gd`-utvidelsene må være installert og aktivert i PHP
- [Composer](https://getcomposer.org) må være installert
- mPDF-programmet må være installert ([veiledning for installasjon](http://mpdf.github.io/installation-setup/installation-v7-x.html))

## Installasjon
For at programmet skal fungere må mPDF være installert.
Her er en rask veiledning for installasjon:

### 1. Opprett en mappe for prosjektet ditt
Opprett en mappe, for eksempel i `/var/www/`, der prosjektfilene lagres.
```
$ mkdir /var/www/politiskfravaer
$ cd /var/www/politiskfravaer
```
Om du får tillatelsesproblemer, kan det være en idé å bruke `sudo`, men prøv uten først.

### 2. Installer mPDF i mappen
mPDF må installeres i selve prosjektmappen. Dette gjøres med Composer.
```
$ composer require mpdf/mpdf
```
Det er ikke anbefalt å bruke `sudo` med composer. Om du har problemer med å installere programmet, er det mulig å [gjøre det uten composer](http://mpdf.github.io/installation-setup/using-without-composer.html), men dette er heller ikke anbefalt.

### 3. Last ned prosjektfilene
Forsikre deg om at du er i riktig mappe før du laster ned prosjektfilene fra GitHub. Flytt så filene til riktig mappe.
```
$ git clone https://github.com/vt-su/politiskfravaer
$ cd politiskfravaer
$ mv * ..
$ cd ..
$ rm -rd politiskfravaer
```

### Tilleggskonfigurasjon
- [Husk å konfigurere webserveren din (Apache) til å peke mot prosjektmappen.](https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-18-04)
- [Installer et sertifikat for å bruke tjenesten med HTTPS.](https://certbot.eff.org) **Dette er av sikkerhetsgrunner sterkt anbefalt.**

## Feilsøking
### Siden er blank
Hvis du får en blank side i stedet for et PDF-dokument, prøv følgende: Kontroller at filtillatelser er riktige.
```

```
