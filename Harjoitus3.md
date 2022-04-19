# Harjoitus 3 - Versionhallinta

Tämän tehtävän harjoitukset on tehty samalla kokoonpanolla kuin aiemmissakin harjoituksissa.

## z) Lue ja tiivistä artikkeli muutamalla ranskalaisella viivalla. Tässä z-alakohdassa ei tarvitse siis tehdä testejä tietokoneella.

### [Commonmark contributors: Markdown Reference](https://commonmark.org/help/) (huomaa ainakin otsikot risuaidoilla, kappalejako tyhjällä rivillä, sisennys (tab) koodia, lista, linkki, kuva.)

- Markdown on yksinkertainen työkalu tekstin muokkaamiseen
- Tekstiä voi muokata \*-merkeillä. \**kursivoi\** ja \*\***lihavoi***\*
- "#" tekstin edessä tekee siitä otsikon. Risuaitojen määrä kertoo otsikon tason (# - pääotsikko, ## - alaotsikko jne.)
- Tyhjä rivi muodostaa tekstiin kappalejaon
- Painamalla kerran tab-näppäintä saa tehtyä tekstiin sisennyksen. Sisennyksessä oleva teksti näytetään erillisenä "koodilohkona"
```    
	santtu@massina:~/palvelintenhallinta$ ls -la
	total 44
	drwxr-xr-x  3 santtu santtu  4096 18. 4. 11:53 .
	drwxr-xr-x 18 santtu santtu  4096 18. 4. 11:48 ..
	drwxr-xr-x  8 santtu santtu  4096 18. 4. 11:58 .git
	-rw-r--r--  1 santtu santtu   740 18. 4. 12:06 Harjoitus3.md
	-rw-r--r--  1 santtu santtu 18092 18. 4. 11:48 LICENSE
	-rw-r--r--  1 santtu santtu    39 18. 4. 11:48 README.md
	-rw-r--r--  1 santtu santtu   166 18. 4. 11:48 TESTI.md
```
- Tavallisen listan voi muodostaa laittamalla tekstin eteen merkin `* tai -` 
- Numeroidun listan voi muodostaa laittamalla tekstin eteen `1. tai 1)`
- Linkin saa luotua seuraavasti: `[Linkin nimi](url-osoite)`
- Kuvan saa lisättyä seuraavasti: `![Kuvan nimi](kuvan osoite)`

## a) MarkDown. Tee tämän tehtävän raportti MarkDownina. Helpointa on tehdä raportti GitHub-varastoon, jolloin md-päätteiset tiedostot muotoillaan automaattisesti. Tyhjä rivi tekee kappalejaon, risuaita ‘#’ tekee otsikon, sisennys merkitsee koodinpätkän.

Tämän tehtävän raportti löytyy GitHubista: [Palvelinten hallinta - Harjoitus 3](https://github.com/santtuhurri/palvelintenhallinta/blob/main/Harjoitus3.md)

## b) Pull first. Tee useita muutoksia git-varastoosi. Tee muutama muutos, jossa yksi commit koskee useampaa tiedostoa. Anna hyvä kuvaukset (commit message), yksi englanninkielinen lause imperatiivissa (määräysmuodossa) "Add top level menu to Foobar synchronizer"

Aloitin muutosten tekemisen poistamalla koodi.md nimisen tiedoston, jota käytin apuna "koodilohkon" luomisessa, eikä se enää tässä vaiheessa ollut tarpeellinen.
Seuraavaksi muokkasin TESTI.md tiedostoa, jonka avulla kokeilin vielä aiemmin opittuja Markdownin ominaisuuksia, kuten fontin muokkaamista sekä numeroidun listan tekemistä.
Lopuksi kirjoitin vielä päivityksiä Harjoitus3.md tiedostoon ja aloitin kirjoittamaan tätä osiota.

Tähän kohtaan halusin myös lisätä kuvan 'git commit' kohdasta ja kohtasin lieviä vaikeuksia kuvan lisäämisessä. Apua hain [Stack Overflowsta](https://stackoverflow.com/questions/41604263/how-do-i-display-local-image-in-markdown) ja vaikka kaikki näytti olevan niin kuin pitää, ei kuva silti näkynyt GitHubissa.
Lopulta tajusin, että yritin lisätä kuvaa, joka sijaitsi vain ja ainoastaan Windows-pöytäkoneellani.
Siirsin siis kuvan henkilökohtaisen pilven kautta Linux-virtuaalikoneelleni, loin GitHub arkistoni alle uuden "Images" nimisen kansion johon lisäsin kuvan ja sain sen onnistuneesti näkyviin.

![screenshotOfCommits](Images/gitcommit.jpg)

## b) Kaikki kirjataan. Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.

'git log' näyttää kaikki tehdyt muutokset, jotka on viety loppuun 'git commit' komennolla. Ylhäällä lukee muutoksen commit-tunniste, tämän alapuolella muutoksen tekijän nimi sekä sähköposti.
Sen jälkeen ilmoitetaan muutoksen ajankohta ja viimeisenä lukee vielä 'commit message' eli muutoksen tekijän viesti, siitä mitä muutos pitää sisällään.
Tästä lokitiedostosta käy hyvin ilmi ongelmat kuvan lisäämisen kanssa.

![screenshotOfLog](Images/gitlog.jpg)

'git diff' näyttää kaikki eroavaisuudet versioiden välillä, kunnes käytetään komentoa 'git add .'.
Aluksi ilmoitetaan mistä tiedostosta on kyse ja '@@'-merkkien välissä olevat numerot kertovat mistä rivistä alkaen ja kuinka monta riviä muutos sisältää.
Valkoinen teksti ei ole muuttunut, punainen teksti ja '-' -merkki kertovat poistetuista kohdista ja vihreä teksti sekä '+' -merkki kertovat lisätyistä kohdista.

![screenshotOfDiff](Images/gitdiff.jpg)

'git blame' toimii vain yksittäisen tiedoston kohdalla, esim. 'git blame TESTI.md'.
Se kertoo yksityiskohtaisesti tiedostoon tehdyt muutokset. Numero-kirjainyhdistelmä on muutoksen id, sitä seuraa muutoksen tekijän nimi sekä muutoksen ajankohta.
Seuraavana näkyy rivinumero ja viimeisenä itse rivin sisältö. Tämän avulla on helppo tarkistaa kuka on tehnyt tiedostoon muutoksia ja milloin.

![screenshotOfBlame](Images/gitblame.jpg)

## c) Huppis! Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset --hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.

## d) Formula. Tee uusi salt-tila (formula, moduli, infraa koodina). (Eli uusi tiedosto esim. /srv/salt/terontila/init.sls). Voit tehdä ihan yksinkertaisen parin funktion (pkg, file...) tilan, tai edistyneemmin asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot.

