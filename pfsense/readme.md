# PFsense

PFsense on reititin-palomuuri jakauma/yhdistelmä laite, joka toimii FreeBSD pohjaisen Unix operaattorijärjestelmällä. Pfsense:llä on kaksi tyyppistä avointa lähde sovellusta <b>Community Edition (CE)</b> ja <b>Plus</b> tyyppinen, että ladattavissa fyysiselle työasemille tai virtuaalikoneeseen omistettun reititin-palomuuri verkkoa laitetta. Se voidaan määrittää ja päivittää web-pohjaisen käyttöliittymän kautta, eikä sen hallinta vaadi taustalla olevan FreeBSD-järjestelmän tuntemusta.

- [pfsense](#pfsense)
- [pfsense](#vpn)
- [VPN](#VPN)
  * [ipsec](#ipsec)
    * [pfsense ipsec](#pfsense-ipsec)
    * [Tunnel](#Tunnel)
    * [Phase 1 and 2 settings](#Phase-1-and-2-settings)
  * [openvpn](#openvpn)

- [LDAP](#LDAP)


# VPN

## ipsec

IP Security Architecture

Tietoliikenneprotokollan Internet-yhteyksien turvaaminen, joka tarjoaa salauksen, osapuolten todennuksen ja tiedon eheyden varmistamisen. Pääasiassa tämä tarkoittaa UDP-pohjaisia sovelluksia, ICMP-kontrolliviestejä sekä reitityksessä ja tunneloinnissa käytettyjä IP-protokollia kuten GRE:tä, OSPF:aa ja niin edelleen. Verrattaessa kuljetuskerroksen protokolliin (4.layer OSI-malli), kuten SSLään, haittapuolena on se, että IPsec-protokollien pitää pystyä hallitsemaan myös vakaus- ja fragmentoitumisongelmat, jotka yleensä on hoidettu korkeammalla tasolla, TCP- eli kuljetuskerroksella.

IPsec-protokollaa voidaan käyttää VPN-ratkaisun eli näennäisen yksityisverkon rakentamiseen kummallakin tavalla. On huomioitava että saavutettava tietoturva eroaa huomattavasti näiden kahden mallin välillä.

![Alt text](images/IPsec-1.png)

### pfsense ipsec

Pfsense ipsec tunneli

![Alt text](images/pfsense-ipsec-1.PNG)

### Tunnel 

### Phase 1 and 2 settings

## openvpn

Openvpn velhoisuus on pfsense sovelluksen yksi kätevä tapa määrittää etäkäyttö-VPN mobiili asiakkaalle  <b> (remote access) </b>. Ohjattujen konfigurointi/määrityksest kaikki tarvittavat OpenVPN etäkäyttöpalvelimet tarvitsevat edellytyksen:
 - Todennuksen lähteen(source) (paikallinen(local), RAdius-server tai LDAP serverin)
 - Varmentaja (CA = certificate authority)
 - Palvelimen varmenne (A server certificate)
 - OpenVPN palvelinesiintymä (OpenVPN server instance)

Ohjauksen toiminnon lopuss palomuurissa on täysin toimiva palvelin, joka on valmis vastaanottamaan yhteyksiä käyttäjiltä, että tätä palvelinkokooonpanoa voi sitten muuttaa tarpeiden mukaan.

Kun reitittimessäsi on käynnissä VPN-palvelin, nii voi muodostaa yhteyden kotiverkkoon turvallisesti ja päästä käsiksi paikalliseen koneeseen mistä tahansa, ja jopa käyttää koti internetyhteyttä etähallinta laiteella.

![Alt text](images/pfsense-openvpn-1.PNG)

# LDAP

Lightweight Directory Access Protocol, on hakemistonpalvelujen tarkoitettu verkkoprotokolla. Se on tarkoitettu tietojen hakemista verko ylitse keskitettyihin palveluihin. Hakemistopalvelu sisältyvät attribuuttipohjaisia/tiedostoattribuutti tietoja, mutta eivät tue monimutkaisiin päivitystoimintoihin kuten transaktio. 

${{\color{red}HUOM}}$; tässä on pien ero LDAP ja microsoft active directory:n kanssa, mitä yhteistä pelivaraa niillä on.
