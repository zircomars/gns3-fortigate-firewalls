# GNS3

![Alt text](images/2739187_GNS-logo.png)

Graphical Network Simulator-3 - verkko ohjelmisto emulaattori, mitä mahdollistaa virtuaalisten ja todellisten laitteiden yhdistelmän, jota käytetään monimutkaisten verkkojen simulointiin. Myös mahdollista tukea palomuuriin tuotteisiin (fortigate), jotta pitää ladata paketti tiedosto simulaation sisään, jotta voi hyöydyntää harjoittelun.

Jos lataa pohjallisen simulaation fyysiselle työasemalleki <b>GNS3 GUI</b> se on ok tai vaihtoehtoisena on simulaation taakse <b> (GNS3 VM)</b> eli oma fyysisen työasemaan pitää ladata/aktiovida virtuaalikone (virtualbox, vmware tai hyper-v). Mutta gns3 sovelluksen näiden virtuaalisointikone se vain tukee kuin server listattuna, mitä laiteitta voi kuin preferenssi (suuntautuminen) tai kuin integroituna molempiin. Myös molemmat ovat suosittuja välineitä.

Jos vmware tyyppistä niin gns3 tukee vmware esxi/workstation and fusion.

* [laitteistot](#laitteistot)
* [Pikaiset käyttöliittymät](#pikaiset-käyttöliittymät)
* [lisä laiteitta](#lisä-laiteitta)
    * [Laiteen lisäys malleja](#laiteen-lisäys-malleja)
- [gns omia dokumentit ja ohjeita](#gns-omia-dokumentit-ja-ohjeita)
    * [academy](#academy)

![Alt text](images/GNS3-network-1.jpg)

## laitteistot

Simulaatio tukee Cisco laiteistoja mm. <b>c7200 lateitta</b>, <b>juniper</b>, <b>huawei</b>, <b> fortigate</b>, <b> pfsense</b> ja yms brändi merkisiä laiteistoja. Periaattees voi upottaa simulaation sisään, mitä voisi kokeilla kuin realistisena konffauksena, että testaa ennen kuin hankii fyysen laiteiston esim. koti tai paikallisen toimistoon, koska säästäisi rahaa tosi paljon ja tietää miltä se kuin toimii realistisena. Toiminnaltaa toimii kuin realistinen, mutta pitää päällä yhtäjaksoisesti niin se on negatiivisin puoli eli sähköt.

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
VPCS - tarkoittaa tietokonetta ei väliä onko läppäri tai fyysinen tietokone (sellainen iso)

![Alt text](GUI-images/GUI-4.PNG) <br>
<br>

Security devices - <br>
![Alt text](GUI-images/GUI-5.PNG)
<br>

<br>
Pikainen valikko, että löytyy kaikki laitteet, mitä omistaa tai kuin kokonaisuudesssa projektissa tai koko GNS3 sovelluksessa löytyy. Esim. Cisco packet tracer versio X.Y.Z on oletuksena näitä N kpl laiteitta. <br>

![Alt text](GUI-images/GUI-6.PNG)
<br>

- Viimeisenä jos on jotakin muistiinpanoja tai merkintöjä toi ensimmäinen kynä merkkinen näköinen on se.
- Toisena merkkinä on (insert pics) - jotakin raahaataan työasemalta jokin kuva
- Kolmas-viides on piirtämistä, että rajoitettaan esim. tässä alueella X-jotakin tai ympyrä Y-jotakin ja perus viiva (raja)
- Lukkon näköinen, ikään kuin lukittaisi X laitetta vaikkapa reititin tai kone ettei siihen tehdä muutosta.
- Ihan oikealla perus zoom in & out, ja kamera logoinen (screenshot)

![Alt text](GUI-images/GUI-7.PNG) <br>

## lisä laiteitta

<b>new Template</b> - Periaatteessa tuodaan/haetaan/ladataan/ tai importoidaan uutta laiteistoa GNS3 virtuaali tietoliikenne ympäristöön, että siitä suoritettaan selainen harjoitus ennen fyysistä ja realista tekemistä. 

Jos on puuttuvia laitetitta/malleja niin voi ladata sovelluksen kautta, mutta mikäli jos on olemassa oleva tiedosto niin perus "import" X-tiedosto, ja tulee olemaan .gns3a tiedostotyyppi. GNS3:lla on oma <ins>marketplaces</ins>, josta voi hyvin käydä lataa sen tiedosto kansion niin perus upottaa GNS3 virtuaaliympäristöön. Marketplaces löytyy mm. labs, softwares, trainng, pdocasts ja jne.

Manually - tarkoittaa jotakin preferenssiä, että muita tukevia sovelluksia ja tiettyjä järjestelmiä.
<br>
![Alt text](images/template-1.PNG) <br>

Perus oletuksena GNS3 virtuaali tietoliikenne verkko ympäristössä on palomuurit, reititin tai yhdistelmä (reititin-palomuuri), erilliset kytkimet ja jne. Guests tarkoittaa erillisiä laiteita mm. iot, selain (firefox), ubuntu, kali linux, macos ja muita ihmeellisiä laiteistoi/vehkeitä.
<br>
![Alt text](images/template-2.PNG) <br>

Muutama esimerkki laiteitta oletuksena, kun lataa ensimmäisen kerran GNS3:sen sovelluksen pyörimään. Valitse sopiva laite niin sitten vaan "install" ja se lisää laiteen kuin GNS3 käyttöjärjestelmän pohjaan.
<br>
![Alt text](images/template-3.PNG) <br>

<br>

![Alt text](images/template-4.PNG) <br>

Erillinen preferenssi/integraatiota, jos työasemaan on ladattu virtualbox/vmware tai käyttöjärjestelmä docker ja jne.
 <br>
 ![Alt text](images/template-5.PNG)  <br>

### Laiteen lisäys malleja

Usein mietityttää minkä merkkisen brändin laitteen mallin tai sarjan lataisi simulaatio listalle/laitteeksi, että suorittaa sen harjoituksen. Vaikkapa Cisco joku sarja (C7200) reititintä tai (2960) kytkintä, Huawei reititin ar6121, Juniper kytkin EX3300 ja jne (haettu Googelesta), sekä palomuureja taisi olla yksittäinen merkki kuten Fortigate/fortinet tai pfsense, mutta niissä on vain se versio erona, että tukeeko vanhempi versiosta uuteen.

Oletuksena voisi käyttää GNS3 tarjoavia, että lataa (install) niitä malleja tai vaihtoehtona tuoda ulkopuolisia tietty malli. Sekä vaikuttaa reititimeen, että onks siinä tarjolla sitä 10 Gigabit, 1 Gigabit tai FastbitEthernet porttia, tai jopa Serial porttia. 

Pien kertaus Fast Ethernet (FE) on 100 Mbps & Gigabit Ethernet (GE) on 1000 Mbps ja 10 Gigabit Ethernet 10 000 Mbps.

Linkki GNS3 kuinka tarkistaa Cisco emulaatorin, että mitä reititin ja kytkin tukevat tai <ins> ei tue </ins> GNS3 simulaatio ympäristössä. https://docs.gns3.com/docs/emulators/cisco-ios-images-for-dynamips/

<hr>

# gns omia dokumentit ja ohjeita

GNS sovellus tukee työaseman Windows, Mac ja jopa erillinen lataus Linux <br>
https://docs.gns3.com/docs/ <br> 
https://www.gns3.com/software/download <br> 

https://docs.gns3.com/docs/emulators/which-emulators-should-i-use <br>

GNS3 windows lataus ohje<br>
https://docs.gns3.com/docs/getting-started/installation/windows <br> 
<br>

GNS3 Marketplace -> Appliances (template) <br> 
https://www.gns3.com/marketplace/appliances <br> 

## academy

https://gns3.teachable.com/courses



