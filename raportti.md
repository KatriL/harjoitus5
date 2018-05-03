# Palvelinten hallinta h5 29.4.2018 - Git, github ja markdown

**Tehtävänanto saatiin Tero Karvisen sähköpostilla 29.4.2018**

http://terokarvinen.com/2018/aikataulu-%E2%80%93-palvelinten-hallinta-ict4tn022-4-ti-5-ke-5-loppukevat-2018-5p

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

Tämän jälkeen menin osoitteeseen _https://github.com/_ ja kirjauduin sisään. Sitten aloitin uuden "säiliön" (eng. repository)

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/new-reposity-e1525288225998.png "uusi säiliö")

Keksin säiliölle nimen, kirjoitin lyhyen kuvauksen ja valitsin lisenssin repositylle. Laitoin myös täpän kohtaan "Initialize this repository with a README". Sen jälkeen _Create repository_.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/createreposityoikea-e1525288302572.png "create reposity")

Nyt voin kopioida säiliön omalle koneelleni.

# Markdown

b) Julkaise raportti MarkDownilla. Jos käytät GitHub:ia, se tekee muotoilun automaattisesti “.md”-päätteisiin dokumentteihin.

Kun uusi säiliö on luotu, voin kopioida kyseisen säiliön omalle koneelleni komennolla 
	
	_git clone https://github.com/KatriL/harjoitus5.git_

Huom! Tarkista ennen kopiointia, että olet käyttäjän kotikansiossa, etkä pelkästään home kansiossa.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/copyreposity-e1525288503990.png "säiliö kopiointi") ![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/gitclonereposityoikea-e1525288477308.png "clone säiliö")

Nyt voimme mennä luomaan tähän _harjoitus5_ kansioon tiedoston komennolla 

	_nano markdown.md_

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/git-kansiopolku-e1525290997505.png "git-kansiopolku")

Lisäsin tiedostoon seuraavat rivit

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/markdowntesttiedosto-e1525288836752.png "markdowntestitiedosto")

Yksittäinen risuaita merkitsee Heading 1

Kaksi risuaitaa merkitsevät Heading 2

Kolme taas Heading 3

Tab-napin avulla voi tehdä sisennyksiä.

Tallensin tiedoston ctrl+x, y, enter

Tämän jälkeen annan komennot 

	_git add ._ ja _git commit_

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/gitpushandpull-e1525289010965.png "gitpullandpush")

Tässä vaiheessa git pyytää meitä konfiguroimaan keitä olemme, koska en tehnyt tätä gitin asennuksen yhteydessä. Annan sähköpostiosoitteeni ja nimeni komennoilla 

	_git config --global user.email "oma sähköposti"_ ja _git config --global user.name "Oma Nimi"_ 

Nämä ovat sitä varten, jotta voidaan nähdä kuka on tehnyt muutoksia säiliöön.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/gitconfigoikea-e1525289537707.png "gitconfig")

Annan komennot 

	_git add ._ ja _git commit_ 

vielä uudestaan. Nyt saamme kirjoitettua commit tekstin, mihin voimme selittää mitä olemme muuttaneet tiedostossa.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/committeksti-e1525291139283.png "committeksti")

_Git add ._ ja _git commit_ jälkeen annan vielä komennot 

	_git pull && git push_ 

Tässä vaiheessa git kysyy säiliön omistajan käyttäjätunnusta ja salasanaa.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/git-pull-push-e1525289670548.png "gitpullpush")

Nyt tiedosto _markdowntest.md_ pitäisi näkyä githubin säiliössä _harjoitus5_.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/githubmarkdown-e1525289782384.png "github markdown")

# Salt-tila github varastosta

c) Aja oma Salt-tila suoraa git-varastosta. Voit joko tehdä tilan alusta lähtien itse tai forkata <a href="https://github.com/terokarvinen/sirotin">sirottimen</a>.

Olen tehnyt aikaisemmin jo Apachen asennuksen salt-tilan githubiin, https://github.com/KatriL/schooltest, joten päätin ajaa sen. Tässä _schooltest_-kansiossa on _high.sh_-tiedosto, jossa on seuraavat rivit:

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/highstate-github-e1525293023639.png "highstategithub")

_Schooltest_-kansiossa olen tehnyt myös _srv/salt_-kansion, jossa on _top.sls_-tiedosto ja _apache_-kansio. Apache-kansiossa on _init.sls_-tiedosto.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/top-sls-e1525293118643.png "top.sls") ![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/apacheinit-e1525293206176.png "apacheinit")

Kopioin komennolla 

	_git clone https://github.com/KatriL/schooltest.git_  käyttäjän xubuntu kotikansiossa. 

Sinne kopioituu _schooltest_-kansio.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/schooltestgithub-e1525290165340.png "schooltestgithub") ![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/git-clone-schooltest-e1525290124266.png "git-clone-schooltest")

Voin mennä katsomaan mitä tiedostoja _schooltest_-kansiossa on. Kaikki tiedostot ja kansiot ovat siirtyneet githubista omalle koneelleni.

Testasin onko Apache asennettuna koneelleni.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/apacheeitoimi-e1525290303869.png "apacheeitoimi")

Voin nyt ajaa tämän tilan highstate komennolla 

	_sudo bash high.sh_ 

paikallisesti ollessani _schooltest_-kansiossa.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/sudo-bash-e1525290254312.png "sudo-bash")

State tila ajetaan ja nyt Apachen tulisi toimia. Testasin vielä Apachen lopuksi.

![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/statemenilc3a4pi-e1525290350270.png "state") ![alt text](https://katrilaulajainen.files.wordpress.com/2018/05/apachetoimii-e1525290334244.png "apachetoimii")


# LÄHTEET:

Karvinen, Tero: Oppitunnit 2018-4-24, Palvelinten hallinta-kurssi

http://terokarvinen.com/2018/aikataulu-%E2%80%93-palvelinten-hallinta-ict4tn022-4-ti-5-ke-5-loppukevat-2018-5p

http://terokarvinen.com/2016/publish-your-project-with-github

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#images
