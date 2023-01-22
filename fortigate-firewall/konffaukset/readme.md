# Fortigate (LAN, WAN, DHCP, Policy)
CLI konffaukset

* [Single port](#Single-port)
* [LAN](#LAN)
* [WAN](#WAN)
* [DHCP](#DHCP)
* [Policy](#Policy)
* [NAT public ip](#NAT-public-ip)
* [NAT Port](#NAT-Port)
* [Backup config](#Backup-config)
* [muu tarkempaa ohjeet](#muu-tarkempaa-ohjeet)
* [](#)

## Single port
Yksittäisen porttien konffaus

config system interface <br>
  edit [porttiNumero] <br>
  set ip [ip-address] [netmask] <br>
  set allowaccess (http https ping ssh telnet) <br>
end <br>
where:

<b>Esimerkki malli:</b>
config system interface <br> 
 edit port1 <br>
 set ip 192.168.100.159 255.255.255.0 <br>
 set allowaccess ping https ssh <br>
end <br>

## LAN

## WAN

## DHCP

## Policy

<hr>

## NAT public ip

## NAT Port

## Backup config

Backup konffi tapahtuu kun palomuuri reititin tai kytkin itsensä menee esim. laite hajoaa, kärähtyy, laite vaihto itsensä (vanhasta uutteen) tai laite x-malli tukee toisensa y-laiteelle. Backup/varmuuskopio pitää olla aina tallella, jotta seuraava laitetta voi suoriutua mahdollisimman nopeasti. 

Suorittamisen keinoja on monipuolista forigate:llä, että klikkauksella käyttöliittymien kautta tai fortigate cli komennon kautta.




## muu tarkempaa ohjeet
https://www.youtube.com/watch?v=xx-_yn2-UXc
