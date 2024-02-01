# Rola `web_srv`

Ta rola służy do instalacji prostego webserwera `lighttpd`. Podstawowe założenia:

- opcjonalnie utworzy LVM na wskaznych PV i zamontouje filesystem w `/var/www`
- zainstaluje paczki serwera lighttpd
- wrzuci dropiny konfiguracyjne:
    - `dirlisting.conf` zezwala na przeglądanie wskazanych katalogów (directory browsing)

        **Pomysł** - a gdyby lista katalogów była listą podaną przez zmienną ? 

- otwiera porty `http` i `https` w firewallu. 
- przywraca kontekst SELinuxa (`restorecon`)

