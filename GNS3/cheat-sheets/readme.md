# Cheat sheets

Tänne tulee poikkeukset cheat sheet:it mm. kuinka annettaan koneelle yksittäinen ip-osoite ja vähä kuin suorittaisi console järjestelmän (cmd)


## VPCS / PC

PC koneelle perus syötettään kysymysmerkki niin antaa/toistaa vaihtoehtoisia valintoja, mitä ollaan hakemassa, myös esim. vaikappa koneelle ip-osoite määrits

![Alt text](images/GNS-PC-cs-1.PNG)

![Alt text](images/GNS-PC-cs-2.PNG)

Pieni listaus taulukko yleis arkipv tarkistaa PC koneen komennot

| Komennot | kuvaus | 
| ------- | ------- |
| $ip [add] [mask] [GW] | tietokoneelle (VPCS) yksittäinen kiinteä ip-osoite esim. <br> $ip 192.168.10.2 255.255.255.0 192.168.10.1 <br><br>  GW eli gateway, muita esimerkkejä <br> $ip 192.168.10.13/24 192.168.10.1  |
| $show ip | tarkista yksittäisen konen kiinteä ip-osoite, gw, dns, mac ja jne. esim; <br><br> NAME : PC3[1] <br> IP/MASK : 192.168.10.13/24 <br> GATEWAY : 192.168.10.1 <br> DNS : <br> MAC : 00:50:79:66:68:02 <br> LPORT : 10010 <br> RHOST:PORT : 127.0.0.1:10011 <br> MTU: : 1500 |
| $show arp | tarkista yksittäisen koneen arp taulukko, mikä periaatteessa tarkoittaa mitä kyseisen koneen kanssa on pinggattu yhteytä vaikappa Kone-A pinggasi Kone-B, C ja jne. <br><br> esim; <br> 00:50:79:66:68:00 192.168.10.10 expires in 83 seconds | 
| $save | tarvittaessa kantsii tallentaa määritetty koneelle se ip-osoite, että tietää seuraavan kerran niin ei tarvi tehdä suurta metsästystä paitsi tarkistaa ip-osoite eli $show ip