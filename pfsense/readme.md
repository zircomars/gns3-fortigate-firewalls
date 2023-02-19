# PFsense

PFsense on reititin-palomuuri jakauma/yhdistelmä laite, joka toimii FreeBSD pohjaisen Unix operaattorijärjestelmällä. Pfsense:llä on kaksi tyyppistä avointa lähde sovellusta <b>Community Edition (CE)</b> ja <b>Plus</b> tyyppinen, että ladattavissa fyysiselle työasemille tai virtuaalikoneeseen omistettun reititin-palomuuri verkkoa laitetta. Se voidaan määrittää ja päivittää web-pohjaisen käyttöliittymän kautta, eikä sen hallinta vaadi taustalla olevan FreeBSD-järjestelmän tuntemusta.

- [pfsense](#pfsense)
- [pfsense](#vpn)
  * [ipsec](#ipsec)
    * [Tunnel](#Tunnel)
    * [Phase 1 and 2 settings](#Phase-1-and-2settings)
  * [openvpn](#openvpn)

- [LDAP](#LDAP)


# VPN

## ipsec

### Tunnel 

### Phase 1 and 2 settings

## openvpn

Openvpn velhoisuus on pfsense sovelluksen yksi kätevä tapa määrittää etäkäyttö-VPN mobiili asiakkaalle  <b> (remote access) </b>. Ohjattujen konfigurointi/määrityksest kaikki tarvittavat OpenVPN etäkäyttöpalvelimet tarvitsevat edellytyksen:
 - Todennuksen lähteen(source) (paikallinen(local), RAdius-server tai LDAP serverin)
 - Varmentaja (CA = certificate authority)
 - Palvelimen varmenne (A server certificate)
 - OpenVPN palvelinesiintymä (OpenVPN server instance)

Ohjauksen toiminnon lopuss palomuurissa on täysin toimiva palvelin, joka on valmis vastaanottamaan yhteyksiä käyttäjiltä, että tätä palvelinkokooonpanoa voi sitten muuttaa tarpeiden mukaan.

![Alt text](images/pfsense-openvpn-1.PNG)

# LDAP

Lightweight Directory Access Protocol, on hakemistonpalvelujen tarkoitettu verkkoprotokolla. Se on tarkoitettu tietojen hakemista verko ylitse keskitettyihin palveluihin. Hakemistopalvelu sisältyvät attribuuttipohjaisia/tiedostoattribuutti tietoja, mutta eivät tue monimutkaisiin päivitystoimintoihin kuten transaktio. 

${{\color{red}HUOM}}$; tässä on pien ero LDAP ja microsoft active directory:n kanssa, mitä yhteistä pelivaraa niillä on.
