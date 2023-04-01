# GNS3

![Alt text](images/2739187_GNS-logo.png)

Graphical Network Simulator-3 - verkko ohjelmisto emulaattori, mitä mahdollistaa virtuaalisten ja todellisten laitteiden yhdistelmän, jota käytetään monimutkaisten verkkojen simulointiin. Myös mahdollista tukea palomuuriin tuotteisiin (fortigate), jotta pitää ladata paketti tiedosto simulaation sisään, jotta voi hyöydyntää harjoittelun.

Jos lataa pohjallisen simulaation fyysiselle työasemalleki <b>GNS3 GUI</b> se on ok tai vaihtoehtoisena on simulaation taakse <b> (GNS3 VM)</b> eli oma fyysisen työasemaan pitää ladata/aktiovida virtuaalikone (virtualbox, vmware tai hyper-v). Mutta gns3 sovelluksen näiden virtuaalisointikone se vain tukee kuin server listattuna, mitä laiteitta voi kuin preferenssi (suuntautuminen) tai kuin integroituna molempiin. Myös molemmat ovat suosittuja välineitä.

Jos vmware tyyppistä niin gns3 tukee vmware esxi/workstation and fusion.

* [laitteistot](#laitteistot)
- [gns omia dokumentit ja ohjeita](#gns-omia-dokumentit-ja-ohjeita)
    * [gns muita cheat sheet](#gns-muita-cheat-sheet)

![Alt text](images/GNS3-network-1.jpg)

## laitteistot

Simulaatio tukee Cisco laiteistoja mm. <b>c7200 lateitta</b>, <b>juniper</b>, <b> fortigate</b>, <b> pfsense</b> ja yms brändi merkisiä laiteistoja. Periaattees voi upottaa simulaation sisään, mitä voisi kokeilla kuin realistisena konffauksena, että testaa ennen kuin hankii fyysen laiteiston esim. koti tai paikallisen toimistoon, koska säästäisi rahaa tosi paljon ja tietää miltä se kuin toimii realistisena. Toiminnaltaa toimii kuin realistinen, mutta pitää päällä yhtäjaksoisesti niin se on negatiivisin puoli eli sähköt.

## Pikaiset käyttöliittymät

Pikainen lyhyt GUI (graphical user interface) graafinen käyttöliittymät

Perus vasemman käyttöliittymmä, josta löytyy useita laiteita mm. reititin/palomuuri, kytkimet, pilvi, nat:taus, tietokone ja jne. Sekä kuinka yhdistää/liittää tietokonen kytkimelle tai muu laiteelle. Jokaisessa näiden 5-nappista (ylhältä laskien) niin löytyy <b>New Template</b>, eli malleja josta tuoo esim. tietoverkkojen brändi tuoteita GNS3 simulaatioon sovellukseen suorittamaan harjoituksen kuin realistisessa elämässä, mutta ongelmana ehkä voi olla jotakin puuttuvia osia että ei mee ihan 100% sama kuin tosi elämässä..

Viimeisenä tommoinen käärme / verkkoliitin näköinen on, että liitettään laite x --> johonkin laite y:hyn. <br>
![Alt text](GUI-images/GUI-1.PNG)

<br>
Routers eli reitittimiä, palomuureja tai yhdistelmä reititin-palomuuri <br>
![Alt text](GUI-images/GUI-2.PNG)
<br>

Kytkimet <br>
![Alt text](GUI-images/GUI-3.PNG)
<br>

<br>
Erilliset pilvet , nat?

![Alt text](GUI-images/GUI-4.PNG) <br>
<br>

Security devices - <br>
![Alt text](GUI-images/GUI-5.PNG)
<br>

<br>
Pikainen valikko, että löytyy kaikki laitteet, mitä omistaa tai kuin kokonaisuudesssa projektissa tai koko GNS3 sovelluksessa löytyy. Esim. Cisco packet tracer versio X.Y.Z on oletuksena näitä N kpl laiteitta. <br>
![Alt text](GUI-images/GUI-6.PNG)
<br>

## lisä laiteitta

<b>new Template</b>
Periaatteessa tuodaan/haetaan/ladataan/ tai importoidaan uutta laiteistoa GNS3 virtuaali tietoliikenne ympäristöön, että siitä suoritettaan selainen harjoitus ennen fyysistä ja realista tekemistä. 

Jos on puuttuvia laitetitta/malleja niin voi ladata sovelluksen kautta, mutta mikäli jos on olemassa oleva tiedosto niin perus "import" X-tiedosto, ja tulee olemaan .gns3a tiedostotyyppi. 

Manually - tarkoittaa jotakin preferenssiä, että muita tukevia sovelluksia ja tiettyjä järjestelmiä.
<br>
![Alt text](images/template-1.PNG) <br>

Perus oletuksena GNS3 virtuaali tietoliikenne verkko ympäristössä on palomuurit, reititin tai yhdistelmä (reititin-palomuuri), erilliset kytkimet ja jne. Guests tarkoittaa erillisiä laiteita mm. iot, selain (firefox), kali linux, macos ja muita ihmeellisiä laiteistoi/vehkeitä.
<br>
![Alt text](images/template-2.PNG) <br>

Muutama esimerkki kuvakaappaus 
<br>
![Alt text](images/template-3.PNG) <br>

<br>
![Alt text](images/template-4.PNG) <br>

Erillinen preferenssi/integraatiota, jos työasemaan on ladattu virtualbox/vmware tai käyttöjärjestelmä docker ja jne.
 <br>
 ![Alt text](images/template-5.PNG)  <br>

# gns omia dokumentit ja ohjeita

https://docs.gns3.com/docs/ <br> 
https://gns3.com/marketplace/appliances <br>

https://docs.gns3.com/docs/emulators/which-emulators-should-i-use <br>

GNS3 windows lataus ohje<br>
https://docs.gns3.com/docs/getting-started/installation/windows 
<br>
GNS3 Marketplace -> Appliances (template)
https://www.gns3.com/marketplace/appliances