# Harjoitus 3 - Versionhallinta

## z) Lue ja tiivistä artikkeli muutamalla ranskalaisella viivalla. Tässä z-alakohdassa ei tarvitse siis tehdä testejä tietokoneella.

### [Commonmark contributors: Markdown Reference](https://commonmark.org/help/) huomaa ainakin otsikot risuaidoilla, kappalejako tyhjällä rivillä, sisennys (tab) koodia, lista, linkki, kuva.

- Markdown on yksinkertainen työkalu tekstin muokkaamiseen
- Tekstiä voi muokata \*-merkeillä. \**kursivoi\** ja \*\***lihavoi***\**
- 	*Tämä teksti on kursivoitua*
- 	**Tämä teksti on lihavoitua**
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
- Listoja voi muodostaa laittamalla tekstin eteen merkin * tai - 
