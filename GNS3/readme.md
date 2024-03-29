# GNS3

![Alt text](images/2739187_GNS-logo.png)

Graphical Network Simulator-3 - verkko ohjelmisto emulaattori, mitä mahdollistaa virtuaalisten ja todellisten laitteiden yhdistelmän, jota käytetään monimutkaisten verkkojen simulointiin. Myös mahdollista tukea palomuuriin tuotteisiin (fortigate), jotta pitää ladata paketti tiedosto simulaation sisään, jotta voi hyöydyntää harjoittelun.

Jos lataa pohjallisen simulaation fyysiselle työasemalleki <b>GNS3 GUI</b> se on ok tai vaihtoehtoisena on simulaation taakse <b> (GNS3 VM)</b> eli oma fyysisen työasemaan pitää ladata/aktiovida virtuaalikone (virtualbox, vmware tai hyper-v). Mutta gns3 sovelluksen näiden virtuaalisointikone se vain tukee kuin server listattuna, mitä laiteitta voi kuin preferenssi (suuntautuminen) tai kuin integroituna molempiin. Myös molemmat ovat suosittuja välineitä.

Jos vmware tyyppistä niin gns3 tukee vmware esxi/workstation and fusion.

* [laitteistot](#laitteistot)
* [Pikaiset käyttöliittymät](#pikaiset-käyttöliittymät)
* [lisä laiteitta](#lisä-laiteitta)
    * [Laiteen lisäys malleja](#laiteen-lisäys-malleja)
    * [materiaalien tuominen](#materiaalien-tuominen)

- [muita gns ongelmia](#muita-gns-ongelmia)
    * [virtualikone integrointi](#virtualikone-integrointi)
    * [oma työasema cpu](#oma-työasema-cpu)
    * [Cisco IOU license](#cisco-iou-license)

- [gns omia dokumentit ja ohjeita](#gns-omia-dokumentit-ja-ohjeita)
    * [academy](#academy)
        * [muita ohjeita jos puuttuu](#muita-ohjeita-jos-puuttuu)
            * [GNS3, remote server and virtualbox (more cpu and ram) and other](#gns3-remote-server-and-virtualbox-more-cpu-and-ram-and-other)
    * [templates ja application laiteitta ](#templates-ja-application-laiteitta)

![Alt text](images/GNS3-network-1.jpg)

## laitteistot

Simulaatio tukee Cisco laiteistoja mm. <b>c7200 lateitta</b>, <b>juniper</b>, <b>huawei</b>, <b> fortigate</b>, <b> pfsense</b> ja yms brändi merkisiä laiteistoja. Periaattees voi upottaa simulaation sisään, mitä voisi kokeilla kuin realistisena konffauksena, että testaa ennen kuin hankii fyysen laiteiston esim. koti tai paikallisen toimistoon, koska säästäisi rahaa tosi paljon ja tietää miltä se kuin toimii realistisena. Toiminnaltaa toimii kuin realistinen, mutta pitää päällä yhtäjaksoisesti niin se on negatiivisin puoli eli sähköt.

## Pikaiset käyttöliittymät

Pikainen lyhyt GUI (graphical user interface) graafinen käyttöliittymät

Perus vasemman käyttöliittymmä, josta löytyy useita laiteita mm. reititin/palomuuri, kytkimet, pilvi, nat:taus, tietokone ja jne. Sekä kuinka yhdistää/liittää tietokonen kytkimelle tai muu laiteelle. Jokaisessa näiden 5-nappista (ylhältä laskien) niin löytyy <b>New Template</b>, eli malleja josta tuoo esim. tietoverkkojen brändi tuoteita GNS3 simulaatioon sovellukseen suorittamaan harjoituksen kuin realistisessa elämässä, mutta ongelmana ehkä voi olla jotakin puuttuvia osia että ei mee ihan 100% sama kuin tosi elämässä..

Viimeisenä tommoinen käärme / verkkoliitin näköinen on, että liitettään laite x --> johonkin laite y:hyn. <br>
![Alt text](GNS-GUI-images/GUI-1.PNG)

<br>
Routers eli reitittimiä, palomuureja tai yhdistelmä reititin-palomuuri <br>

![Alt text](GNS-GUI-images/GUI-2.PNG)
<br>

Kytkimet <br>
![Alt text](GNS-GUI-images/GUI-3.PNG)
<br>

<br>
Erilliset pilvet , nat? 
VPCS - tarkoittaa tietokonetta ei väliä onko läppäri tai fyysinen tietokone (sellainen iso)

![Alt text](GNS-GUI-images/GUI-4.PNG) <br>
<br>

Security devices - <br>
![Alt text](GNS-GUI-images/GUI-5.PNG)
<br>

<br>
Pikainen valikko, että löytyy kaikki laitteet, mitä omistaa tai kuin kokonaisuudesssa projektissa tai koko GNS3 sovelluksessa löytyy. Esim. Cisco packet tracer versio X.Y.Z on oletuksena näitä N kpl laiteitta. <br>

![Alt text](GNS-GUI-images/GUI-6.PNG)
<br>

- Viimeisenä jos on jotakin muistiinpanoja tai merkintöjä toi ensimmäinen kynä merkkinen näköinen on se.
- Toisena merkkinä on (insert pics) - jotakin raahaataan työasemalta jokin kuva
- Kolmas-viides on piirtämistä, että rajoitettaan esim. tässä alueella X-jotakin tai ympyrä Y-jotakin ja perus viiva (raja)
- Lukkon näköinen, ikään kuin lukittaisi X laitetta vaikkapa reititin tai kone ettei siihen tehdä muutosta.
- Ihan oikealla perus zoom in & out, ja kamera logoinen (screenshot)

![Alt text](GNS-GUI-images/GUI-7.PNG) <br>

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

Erillinen preferenssi/integraatiota, jos työasemaan on ladattu virtualbox/vmware tai käyttöjärjestelmä docker ja jne. Sitten siinä yhdessä valikoimasta on teema muutaminen. Myös kun suorittaa vaikkapa pc, reititin tai kytkimen asetukset muutamista just sitä komento antamista niin se console suoriuttuu kuin realisistinen putty näkymä (kuin identtinen), että perus muokkaa näkymän teeman vähä isommaksi.
 <br>
 ![Alt text](images/template-5.PNG)  <br>

### Laiteen lisäys malleja

Usein mietityttää minkä merkkisen brändin laitteen mallin tai sarjan lataisi simulaatio listalle/laitteeksi, että suorittaa sen harjoituksen. Vaikkapa Cisco joku sarja (C7200) reititintä tai (2960) kytkintä, Huawei reititin ar6121, Juniper kytkin EX3300 ja jne (haettu Googelesta), sekä palomuureja taisi olla yksittäinen merkki kuten Fortigate/fortinet tai pfsense, mutta niissä on vain se versio erona, että tukeeko vanhempi versiosta uuteen.

Oletuksena voisi käyttää GNS3 tarjoavia, että lataa (install) niitä malleja tai vaihtoehtona tuoda ulkopuolisia tietty malli. Sekä vaikuttaa reititimeen, että onks siinä tarjolla sitä 10 Gigabit, 1 Gigabit tai FastbitEthernet porttia, tai jopa Serial porttia. 

Pien kertaus Fast Ethernet (FE) on 100 Mbps & Gigabit Ethernet (GE) on 1000 Mbps ja 10 Gigabit Ethernet 10 000 Mbps.

Linkki GNS3 kuinka tarkistaa Cisco emulaatorin, että mitä reititin ja kytkin tukevat tai <ins> ei tue </ins> GNS3 simulaatio ympäristössä. https://docs.gns3.com/docs/emulators/cisco-ios-images-for-dynamips/

### materiaalien tuominen

GNS3 materiaalien tuomisessa saattaa joskus tuottaa epäonnistumista eli ettei ne toimi, sekä puuttuu jotakin konffauksia, määrityksiä ja jne. ettei se simulaatio ymmärrä sitä tuonneen mallin merkkiä mm. jupiter, cisco, huawei ja jne erilaisia brändi merkkeistä. 

Kun usein katsoo Youtube videoista, että miten <ins>he</ins> ovat tuonneet ja onnistuneet saamaan sitä materiaalia sinne omaan simulaatio pohjaan niin se toimii heillä, mutta se ei tarkoita 100% toimisi itsellä. Koska simulaatiot näiden lähdekoodit päivittyvät vuosittain, että tukeeko sitä esim. n. alle/yli vuoden vanhan video ohjeen mukaan. Tai vaihtoehtona katsoo muista bloggista (github) ja jne ohjeita. Ongelmista tietenkin aina esiintyy ja pitää taistella/hakkaa päättä seinään, että saisi jotenkin suostumaan ja lisämään siihen simulaatio pohjaan sitä tiettyä/puuttuvaa materiaalia sisään.. 

<hr>

# muita gns ongelmia

Ongelmia voi mahdollista olla, että yrittää saada upotettua lisä laiteistoja GNS3 simulaatio sovellukselle ja sieltä jatkaa eteenpäin, mutta usein jatkuvasti <b>new templates:sta</b> --> siitä kun yritettään "install an appliance from the GNS3 server" niin tuotaa herjaamista. 

![Alt text](images/gns-problem-1.PNG)

Vaihtoehtona se tarvii jopa virtuaalikoneen serverin, jotta saisi pelittämään yhteytä vähä kuin integrointia.

## virtualikone integrointi

GNS3 virtuaalikoneesta vaihtoehtoisia tyyppejä on mm. virtualbox tai vmware ympäristöä, että sisäkkäisen virtualisointituki Intel-suorittimille lisätään, on osoitettava Virtualbox-foorumeille, ei GNS3-käyttäjien foorumeille.

Ennen kuin suoritta mitään niin pitää ladata virtualikoneen oma tarvittava paketti tiedosto, että importaa sen joko <b>vmware:n</b> tai <b>virtualbox</b> koneelle. Koska luodakseen kevyen ja vankan tavan luoda GNS3-topologioita, jotka välttävät useita yleisiä ongelmia, joita esiintyy käytettäessä GNS3:n paikallista asennusta. https://www.gns3.com/software/download-vm 

Tarkista GNS3 käyttöliittymistä kuin Edit -> Preferences ja vasemmasta valikkosta (GNS3 VM) asukset & että sallittaan virtualisointi moottori eli virtualikone ja pidä oletuksena noi tietyt asetukset.

![Alt text](images/gns-problem-2.PNG)

<b> Virtuaalikone vaihde </b> - jos on ladannut virtuaalikoneen työpöytään. Virtualbox sovellus ei ole onneks mikään iso, mutta tarvittavat materiaalit on tosi isoja jopa yli 1GB kapasiteettiä.. 


![Alt text](images/gns-problem-4.PNG)

Virtualkone on päällä nii haettaan (import) ja ladattun GNS3 VM puuttuva osuus.

![Alt text](images/gns-problem-5.PNG)
![Alt text](images/gns-problem-3.PNG)

Tämän jälkeen menee hetki se importtaa sen tiedoston niin jonka jälkeen saa tietyn kuin ip-osoite. Myös kantsii pitää tätä virtuaalikoneen käynnissä, koska mikäli jos tai kun hakee lisää laiteistoja, ja harjoittelee lisä asetuksia mm. leikkii palomuuria, reititystä ja testaa jotakin kuin toimisi tosi elämässä.

![Alt text](images/gns-problem-6.PNG)

Samalla tämä importattu IP-osoite ikäänkuin suorittaisi virtuaalikoneen (server), että voi käydä selailemassa tutkailemassa ja tarkistamassa jänniä asetuksia. Ikäänkuin näyttäisi serverin lokaali sisäiset muistit, perus asetukset (teema) ja jopa löytyy päivitystäkin erikseen.

![Alt text](images/gns-problem-7.PNG)
![Alt text](images/gns-problem-8.PNG)

## oma työasema cpu

GNS3 virtuaalikonen projektien tekemisessä vaikkappa avaa useita console:a tai aktivoida isoa projektia mm. paljon kytkintä, reititintä, palomuuria ja koneita, että vaikuttaa siihen työaseman prosessiin (cpu) ja jopa tehtävänhallintaan (task manager), että miten se jaksaa kantaa ja tukea gns3 simulaatiota.. ehkä mahdollista perus tai sitä tehokampaa konetta hankia mm. inte core 5 tai 7, ei i3, koska ei välttämättä jaksa kantaa ja sykkiä, mikäli jos on tavallinen tietokoneen käyttäjä. Riippuu konen käyttäjästä mihin käyttötarkoitukseen hän käyttämässä.

Kantsii tarkistaa tietyt asetukset kuntoon; Edit/Preferences (GNS3 VM)

Main server (fyysisen työasema) Host binding; 127.0.0.1 on localhost ip-osoite, sekä takana vaihtoehtoisia on mm. polkuna;
localhost, 0.0.0.0 , 127.0.0.1, työaseman verkkokortti eli 192.168.X.Y alkuinen tai vaihtoehtona virtuaalikoneen pohjaisen IP-osoite.

Remote server on just esim. vaikkapa azure virtuaalikkoneiden ympäristön tai jopa virtuaalikoneen (vmware / virtualbox) luoman pohjan importattu tai uusi koneen sen itsensä saanneen IP-osoite 192.168.Y.X ja portti 80 (Http) protokolla.

![Alt text](images/gns-problem-9.PNG)

<br>

Lisäämisessä kantsii lisätä varmuuden vuodeksi virtuaalikoneen IP-osoite, koska antaa GNS3 projektissa/harjoituksessa niin kuin suorittaa sitä prosessoria/cpu:ta, että jaksaa kantaa sitä suorituskykyä ja järjestelmää kuin tukena. Salli authentikointi eli user ; password . Oletuksena käyttis on gns3 ; gns3 

![Alt text](images/gns-problem-10.PNG)

![Alt text](images/gns-problem-12.PNG)

Jos on virtualbox kantsii tarkistaa sen importattu/projekti/vm resurssi.

(Attached to) - valinnasta on moni tyyppisiä, että riippuu mihin käyttötarkoitukseen on käytössä mm. NAT, Bridged networking (silattu verkkoyhteys), Internal-, Host-only, cloud, generic networking ja viimeisenä (not attached).

![Alt text](images/gns-problem-11.PNG)

Virtualbox verkkoyhteys joko nat, silattu yhteys tai yms: https://www.virtualbox.org/manual/ch06.html

## Cisco IOU license

Tietyt jotakin template (laiteistot) ei yhtäkkiä anna sallia käynnistää console (cmd:tä), ettei anna kytkimen  suorittaa harjoitusta/projektia vaikkapa lisäisi vlan id:tä, portti moodia tai muuta kytkimen asetusta.

![Alt text](images/gns-problem-13.PNG)

Suorittamiseen kantsii olla WinSCP työkalu, jolla sen kautta suorittaa avoimen lähdekoodiin SSH-protokollan eli työaseman ja SSH IP-osoite yhteyden vaikappa just tämä virtuaalikone yhteys (virtualbox / vmware) serveri. Tätä on pako suorittaa WinSCP asetuksen työkalun kautta, koska ilman sitä ei menisi ja ei löydy fyysisesti työaseman C-aseman kansiosta tai C-aseman Program Files.

Ennen siirtoa pitää ladata yksi zip paketti tiedosto (muista vielä purkkaa zip tiedosto), josta tarvittaan tämmöinen <b>CiscoIOUKeygen3f.py</b>.
Tiedosto polkuun mihin ollaan siirtämässä (opt/gns3/images/IOU) pitää lisätä tommoinen <b><ins>CiscoIOUKeygen3f.py</ins></b>.

Vasemalla omatyöasema ja oikealla on just se virtuaalikoneen SSH protokolla yhteys. Ennen Winscp liittämistä pitää yhdistää just se virtuaalikoneen gns3 pohjan/serverin IP-osoite ja millä käyttäjätunnus;salasanalla mennään oletuksena käytettään gns3:sta (user & password; gns3)
![Alt text](images/gns-problem-13-1.PNG)

Siirrettyn CiscoIOUKeygen3f.py jälkeen - avaa virtuaalikoneesta (virtualbox / vmware) Shell scripttaus (kuin Linux console) näkymän eli <b>Shell</b>. 

Jonka jälkeen mennään taas polkuun (/opt/gns3/images/IOU), josta näkee sen siirrettyn python tiedoston ja sitten aktivoidaan se tiedosto eli komennolla <b> $sudo python3 CiscoIOUKeygen3f.py </b>. Mikä se ikäänkuin purkkaa sen python tiedoston, ja winscp:stä pitäisi ponnahtaa se <b> iourc.txt </b> tiedosto. Sitten vaan virtuaalikoneen shell scriptauksesta voidaan poistua eli 2x $exit . 

HUOM. ennen kuin lopettaa Winscp protokollan siirron niin kantsii siirtää sen <b> iourc.txt </b> itselle työasemaan.

![Alt text](images/gns-problem-14.PNG)

![Alt text](images/gns-problem-15-2.PNG)

Tästä ohje videosta löytyy usein youtuubestä tai muualta linkkistä: <br>
https://www.youtube.com/watch?v=2QQmbt-l1O0 <br>
https://timigate.com/2021/10/cisco-iou-l2-keygen-license-for-gns3.html  <br>

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

### muita ohjeita jos puuttuu

https://www.youtube.com/watch?v=8VQ8eTmMtjQ <br>
http://commonerrors.blogspot.com/2019/06/gns3-vm-is-not-available.html <br>
https://docs.gns3.com/docs/using-gns3/beginners/switching-and-gns3/ <br>

#### GNS3, remote server and virtualbox (more cpu and ram) and other

https://www.youtube.com/watch?v=kLLIbOHRKiU <br>

IOUS licenses <br>
https://www.youtube.com/watch?v=2QQmbt-l1O0

## templates ja application laiteitta 

https://www.raghededris.com/2022/06/06/free-download-cisco-ios-images-for-gns3-and-eve-ng/ <br>
https://networkrare.com/download-cisco-iou-iol-images-gns3-gns3-iou-vm-oracle-virtual-box-l2-l3-cisco-switch-images/ <br>

https://www.youtube.com/watch?v=nB0iZd9z3CI  <br>

https://github.com/GNS3/gns3-registry/tree/master/appliances <br>
