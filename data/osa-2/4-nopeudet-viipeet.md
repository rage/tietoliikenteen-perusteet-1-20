---
path: '/osa-2/4-nopeudet-viipeet'
title: 'Nopeudet ja viipeet'
---


Tietoliikenteessä puhumme verkon nopeudesta, vaikka tietoliikenneverkko itse ei mihinkään liiku. Verkon nopeus tarkoittaakin oikestaan verkon välityskykyä eli kuinka paljon dataa verkkoa pitkin pystyy siirtymään tietyssä ajassa.


## Verkon nopeus ja viestin kulkuaika


Tietoliikenteessä viestin siirtoon menee aikaa. Tämä aika riippuu toisaalta verkon nopeudesta (bitteinä sekunnissa), viestin pituudesta (bitteinä) ja mahdollisista viivästyksistä matkan varrella.

Yhdessä linkissä viestin siirtoaika on helppo arvioida, kun tiedämme linkin liikennöintinopeuden (bitteinä sekunnissa) ja viestin pituuden (biteissä). Tästä on helppo jakolaskulla (viestin pituus / liikennöintinopeus) saada arvio kyseisen viestin siirron kestolle.

Tietoliikenteessä siirtonopeudet ilmoitetaan aina bitteinä sekunnissa (b/s) ja etuliitteet (katso [wikipedian sivu](https://fi.wikipedia.org/wiki/Mittayksik%C3%B6n_etuliite)) ovat aina aitoja kymmenen potensseja, toisin kuin tiedon tallennuksessa, jossa usein käytetään tavuja ja kakkosen potensseja.

Tietoliikenteessä käytämme aina [SI-järjestelmän mukaisia kerrannaisyksiköitä etuliitteinä](https://fi.wikipedia.org/wiki/Kansainv%C3%A4linen_yksikk%C3%B6j%C3%A4rjestelm%C3%A4#Kerrannaisyksik%C3%B6t). Näistä tärkeimpiä ovat nano, mikro, kilo, mega, giga ja tera.

Viestin kulkua hidastavat muut kuljetettavat viestit. Jos kaksi viestiä pitää siirtää samaa yhteyttä pitkin, niin ne eivät voi mennä yhtä aikaa vaan ne täytyy lähettää peräkkäin. Tällöin niiden yhteinen kokonaissiirtoaika on kummankin viestin siirtoaika yhteensä.

Laskutoimitukset ovat aina arvioita, koska viestit eivät kulje verkossa yksin. Usein näissä karkeissa laskelmissa oletetaan, että muita viestejä ei ole tai että tällä viestillä on käytettävissään tietty osuus koko kapasiteetista. Näillä karkeillakin arvoilla on helppo havaita, onko esimerkiksi järkevää siirtää jokin datamäärä tietyn yhteyden yli. Joskus siihen vain olisi kulumassa liikaa aikaa ja on syytä miettiä muita vaihtoehtoja. Näillä yksinkertaisilla laskutoimituksilla pärjää kotiverkossa, koska se usein on yhtä ja samaa aliverkkoa, jolloin viestin voi siirtää suoraan lähettäjältä vastaanottajalle.

Koska viestit kulkevat paketteina, joissa on mukana eri kerrosten otsakkeet, niin todellinen siirrettävä bittimäärä on suurempi kuin todellinen lähetettävä data. Jos viesteissä on paljon dataa, niin otsakkeiden aiheuttama lisäys ei ole merkityksellinen. Toisaalta, jos viestit ovat erittäin lyhyitä, niin suurin osa siirrettävästä datasta onkin näitä otsaketietoja ja siirto kestää paljon tuota yksinkertaista laskutoimitusta kauemmin.


## Viipeet

Pakettikytkentäisessä verkossa, kuten internet, viestin kulku lähettäjältä vastaanottajalle tapahtuu linkki kerrallaan. Jokaisella linkillä on oma liikennöintinopeutensa. Hitain näistä määrää millä nopeudella viesti voi korkeintaan kulkea. Kotiverkkojen kohdalla hitain linkki on tyypillisesti se, joka yhdistää kotiverkon ja palveluntarjoajan verkon. Siksi kotiverkkojen liikennöintinopeus ajatellaan yleensä tämän linkin nopeudeksi. Kotiverkon sisäinen liikenne voi kuitenkin tapahtua nopeammin.

Matkan varrella olevat reitittimet aiheuttavat tuon edellä kuvatun siirtoajan (tai oikeammin lähetysviiveen) lisäksi vielä vähän lisää viivettä. Viestin käsittelyyn menee hiukan aikaa (prosessointiviive). Lisäksi viesti voi joutua odottamaan linkin vapautumista hetkisen ennen kuin se voidaan lähettää (jonotusviive). Viimeinen viive on etenemisviive, joka ottaa huomioon sen miten kauas viesti on menossa. Nämä viiveet yhdessä muodostavat siirtoviiveen. Koska prosessointiviive, jonotusviie ja etenemisviive ovat huomattavasti lähetysviivettä pienempiä, niin jätämme ne tässä pois ja keskitymme siirtoviiveen laskennassa vain tuohon lähetysviiveeseen.

Ruuhkaisessa verkossa tosin jonotusviive voi olla merkittävä, mutta jätetään nämä ruuhkatilanteisiin liittyvät laskelmat tältä kurssilta pois. Tästä jonotuksesta aiheutuu suuri osa verkossa tapahtuvista pakettien katoamisista.


Tehdään pari hyvin yksinkertaista laskutoimitusta.


<quiz id="6a90011c-96a7-5f91-aa4b-c0ef97de5e2e"></quiz>


<quiz id="443840a0-7729-5923-b1e4-1ebde4a3faf7"></quiz>


<quiz id="4a9446ca-a6de-5d69-8407-a4b476d09c82"></quiz>


## Yhteenveto

Tässä osassa on käyty läpi kotiverkon toiminnan kannalta keskeiset laitteet ja palvelut. Lisäksi on opittu arvioimaan isojenkin datamäärien tarvitsemia siirtoaikoja.

<quiz id="48fbc451-705b-5e84-8ae1-89fe05f18cd1"></quiz>
