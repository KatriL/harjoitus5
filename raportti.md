**Tehtävänanto saatiin Tero Karvisen sähköpostilla 29.4.2018**

(http://terokarvinen.com/2018/aikataulu-%E2%80%93-palvelinten-hallinta-ict4tn022-4-ti-5-ke-5-loppukevat-2018-5p">http://terokarvinen.com/2018/aikataulu-%E2%80%93-palvelinten-hallinta-ict4tn022-4-ti-5-ke-5-loppukevat-2018-5p)

a) Valitse aihe omaksi kurssityöksi ja varaa se kommenttina aikataulusivun perään.

b) Julkaise raportti MarkDownilla. Jos käytät GitHub:ia, se tekee muotoilun automaattisesti “.md”-päätteisiin dokumentteihin.

c) Aja oma Salt-tila suoraa git-varastosta. Voit joko tehdä tilan alusta lähtien itse tai forkata <a href="https://github.com/terokarvinen/sirotin">sirottimen</a>.

**Käytän tehtävässä omaa kannettavaa tietokonettani:**

**Acer Aspire V3-571G**

**Intel Core i7**

**8GiB RAM**

**Käytän Linuxia livetikun avulla, johon on asennettu Xubuntu versio:**

**_xubuntu-16.04.3-desktop-amd64.iso_**

**Muistitikku 4GB USB muistitikku. Livetikku on tehty Linux palvelimet kurssilla keväällä 2018, tässä linkki tikun tekemiseen:** (https://katrilaulajainen.wordpress.com/2018/01/22/linux-h1-18-1-2018/)

Ennen tehtävien aloitusta olen asentanut koneelleni salt-minionin. Ohjeet salt-minion asennukseen löytyvät aikaisemmista tehtävistäni: (https://katrilaulajainen.wordpress.com/2018/04/02/palvelinten-hallinta-h1-27-3-2018/) tai Tero Karvisen sivuilta: (http://terokarvinen.com/2018/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux)

**Linkki minun githubiini:**(https://github.com/KatriL?tab=repositories)

# Git asennus ja github säiliön luonti

Ennen tehtävien aloitusta asensin koneelle git:in komennolla 

	_sudo apt-get -y install git_

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/git-asennus-e1525288081464.png "git asennus")

Tämän jälkeen menin osoitteeseen <a href="https://github.com/"><em>https://github.com/</em></a> ja kirjauduin sisään. Sitten aloitin uuden "säiliön" (eng. repository)

<img class="alignnone size-full wp-image-522" src="https://katrilaulajainen.files.wordpress.com/2018/05/new-reposity-e1525288225998.png" alt="uusi säiliö" width="885" height="850" />

Keksin säiliölle nimen, kirjoitin lyhyen kuvauksen ja valitsin lisenssin repositylle. Laitoin myös täpän kohtaan "Initialize this repository with a README". Sen jälkeen <em>Create repository.</em>

<img class="alignnone size-full wp-image-523" src="https://katrilaulajainen.files.wordpress.com/2018/05/createreposityoikea-e1525288302572.png" alt="säiliön luonti" width="1017" height="790" />

Nyt voin kopioida säiliön omalle koneelleni.
<h1>Markdown</h1>
b) Julkaise raportti MarkDownilla. Jos käytät GitHub:ia, se tekee muotoilun automaattisesti “.md”-päätteisiin dokumentteihin.

Kun uusi säiliö on luotu, voin kopioida kyseisen säiliön omalle koneelleni komennolla <em>git clone https://github.com/KatriL/harjoitus5.git. </em>Huom! Tarkista ennen kopiointia, että olet käyttäjän kotikansiossa, etkä pelkästään home kansiossa.

<img class="alignnone size-full wp-image-524" src="https://katrilaulajainen.files.wordpress.com/2018/05/copyreposity-e1525288503990.png" alt="säiliön kopiointi" width="1020" height="818" /><img class="alignnone size-full wp-image-525" src="https://katrilaulajainen.files.wordpress.com/2018/05/gitclonereposityoikea-e1525288477308.png" alt="git clone" width="913" height="210" />

Nyt voimme mennä luomaan tähän <em>harjoitus5-</em>kansioon tiedoston komennolla <em>nano markdown.md</em>

<img class="alignnone size-full wp-image-544" src="https://katrilaulajainen.files.wordpress.com/2018/05/git-kansiopolku-e1525290997505.png" alt="git kansiopolku" width="1108" height="183" />

Lisäsin tiedostoon seuraavat rivit

<img class="alignnone size-full wp-image-526" src="https://katrilaulajainen.files.wordpress.com/2018/05/markdowntesttiedosto-e1525288836752.png" alt="markdowntesttiedosto" width="1446" height="339" />

# = yksittäinen risuaita merkitsee Heading 1

## = kaksi risuaitaa merkitsevät Heading 2

### = kolme taas Heading 3

Tab-napin avulla voi tehdä sisennyksiä.

Tallensin tiedoston ctrl+x, y, enter

Tämän jälkeen annan komennot <em>git add . </em>ja <em>git commit</em>.

<img class="alignnone size-full wp-image-528" src="https://katrilaulajainen.files.wordpress.com/2018/05/gitpushandpull-e1525289010965.png" alt="git add . ja git commit" width="540" height="59" />

Tässä vaiheessa git pyytää meitä konfiguroimaan keitä olemme, koska en tehnyt tätä gitin asennuksen yhteydessä. Annan sähköpostiosoitteeni ja nimeni komennoilla <em>git config --global user.email "oma sähköposti" </em>ja <em>git config --global user.name "Oma Nimi"</em>. Nämä ovat sitä varten, jotta voidaan nähdä kuka on tehnyt muutoksia säiliöön.

<img class="alignnone size-full wp-image-530" src="https://katrilaulajainen.files.wordpress.com/2018/05/gitconfigoikea-e1525289537707.png" alt="git config" width="1027" height="347" />

Annan komennot <em>git add .</em> ja <em>git commit</em> vielä uudestaan. Nyt saamme kirjoitettua commit tekstin, mihin voimme selittää mitä olemme muuttaneet tiedostossa.

<img class="alignnone size-full wp-image-545" src="https://katrilaulajainen.files.wordpress.com/2018/05/committeksti-e1525291139283.png" alt="commit" width="1191" height="292" />

<em>Git add .</em> ja <em>git commit</em> jälkeen annan vielä komennot <em>git pull && git push</em>. Tässä vaiheessa git kysyy säiliön omistajan käyttäjätunnusta ja salasanaa.

<img class="alignnone size-full wp-image-533" src="https://katrilaulajainen.files.wordpress.com/2018/05/git-pull-push-e1525289670548.png" alt="git pull push" width="998" height="861" />

Nyt tiedosto markdowntest.md pitäisi näkyä githubin säiliössä harjoitus5.

<img class="alignnone size-full wp-image-534" src="https://katrilaulajainen.files.wordpress.com/2018/05/githubmarkdown-e1525289782384.png" alt="git hub markdown" width="988" height="871" />
<h1>Salt-tila github varastosta</h1>
c) Aja oma Salt-tila suoraa git-varastosta. Voit joko tehdä tilan alusta lähtien itse tai forkata <a href="https://github.com/terokarvinen/sirotin">sirottimen</a>.

Olen tehnyt aikaisemmin jo Apachen asennuksen salt-tilan githubiin, joten päätin ajaa sen. Tässä schooltest-kansiossa on high.sh-tiedosto, jossa on seuraavat rivit:

<img class="alignnone size-full wp-image-549" src="https://katrilaulajainen.files.wordpress.com/2018/05/highstate-github-e1525293023639.png" alt="high.sh" width="1003" height="221" />

<em>Schooltest</em>-kansiossa olen tehnyt myös <em>srv/salt</em>-kansion, jossa on <em>top.sls</em>-tiedosto ja <em>apache</em>-kansio. Apache-kansiossa on <em>init.sls</em>-tiedosto.

<img class="alignnone size-full wp-image-550" src="https://katrilaulajainen.files.wordpress.com/2018/05/top-sls-e1525293118643.png" alt="top.sls" width="1000" height="276" /><img class="alignnone size-full wp-image-551" src="https://katrilaulajainen.files.wordpress.com/2018/05/apacheinit-e1525293206176.png" alt="init.sls" width="995" height="554" />

Kopioin komennolla <em>git clone https://github.com/KatriL/schooltest.git</em> käyttäjän xubuntu kotikansiossa. Sinne kopioituu <em>schooltest</em>-kansio.

<img class="alignnone size-full wp-image-536" src="https://katrilaulajainen.files.wordpress.com/2018/05/schooltestgithub-e1525290165340.png" alt="schooltestgithub" width="997" height="909" /><img class="alignnone size-full wp-image-535" src="https://katrilaulajainen.files.wordpress.com/2018/05/git-clone-schooltest-e1525290124266.png" alt="git clone schooltest" width="1268" height="337" />

Voin mennä katsomaan mitä tiedostoja <em>schooltest-</em>kansiossa on. Kaikki tiedostot ja kansiot ovat siirtyneet githubista omalle koneelleni.

Testasin onko Apache asennettuna koneelleni.

<img class="alignnone size-full wp-image-538" src="https://katrilaulajainen.files.wordpress.com/2018/05/apacheeitoimi-e1525290303869.png" alt="apacheeitoimi" width="1389" height="1006" />

Voin nyt ajaa tämän tilan highstate komennolla <em>sudo bash high.sh</em> paikallisesti ollessani <em>schooltest</em>-kansiossa.

<img class="alignnone size-full wp-image-537" src="https://katrilaulajainen.files.wordpress.com/2018/05/sudo-bash-e1525290254312.png" alt="sudo bash" width="623" height="58" />

State tila ajetaan ja nyt Apachen tulisi toimia. Testasin vielä Apachen lopuksi.

[gallery ids="540,539" type="rectangular"]

[gallery ids="540,539" type="square" columns="2"]
<h1>LÄHTEET:</h1>
Karvinen, Tero: Oppitunnit 2018-4-24, Palvelinten hallinta-kurssi

<a href="http://terokarvinen.com/2018/aikataulu-%E2%80%93-palvelinten-hallinta-ict4tn022-4-ti-5-ke-5-loppukevat-2018-5p">http://terokarvinen.com/2018/aikataulu-%E2%80%93-palvelinten-hallinta-ict4tn022-4-ti-5-ke-5-loppukevat-2018-5p</a>

<a href="http://terokarvinen.com/2016/publish-your-project-with-github">http://terokarvinen.com/2016/publish-your-project-with-github</a>

 
