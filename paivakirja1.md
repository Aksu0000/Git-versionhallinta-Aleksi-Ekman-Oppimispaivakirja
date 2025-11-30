# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Aluksi Gitin komennot ja eri tilojen (untracked, staged, modified) käsitteleminen tuntui jokseenkin sekavalta. Oli vaikeaa hahmottaa, miten tiedostot siirtyvät vaiheesta toiseen ja milloin muutokset todella tallentuvat versiohistoriaan. Myös projektien seuraaminen terminaalissa tuntui haastavalta, kun muutokset eivät tule suoraan näkyviin vaan ne pitää hakea esiin eri komennoilla. 

Uusien tiedostojen lisääminen repositorioon ja commitin tekeminen, kun perusajatus add- ja commit-vaiheista selkeni oli helpohkoa. Myös haarojen luominen ja vaihtaminen oli selkeää komentoja kokeilemalla.

Oppimista auttoi eniten käytännön harjoittelu. Kokeilin komentoja monta kertaa ja  katsoin `git status`-tuloksia useasti. Mahdolliset virheet ja niiden korjaaminen (reset, restore) auttoivat ymmärtämään Gitin logiikkaa.  

Esteitä selvitin lukemalla komennon tulosteen huolellisesti ja kokeilemalla varovaisesti erilaisia vaihtoehtoja. Erityisesti haarautumisen ja merge-konfliktien käsittely selkeytyi kokeilemalla erillisiä testihaaroissa. Lisäksi katsoin vinkkejä Youtubesta.


## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
|---------|--------|
| `git init` | Luo tyhjän Git-repositorion nykyiseen hakemistoon. |
| `git status` | Näyttää tiedostojen tilan (tracked, untracked, staged, modified). |
| `git add <tiedosto>` | Lisää tiedoston seuraavaan talletukseen (staging). |
| `git add .` | Lisää kaikki uudet ja muuttuneet tiedostot seuraavaan talletukseen. |
| `git commit -m "<viesti>"` | Tallettaa staged-muutokset versionhallintaan ja liittää niihin viestin. |
| `git log` | Näyttää talletushistorian. |
| `git log --stat` | Näyttää talletushistorian ja lyhyen yhteenvedon muutoksista. |
| `git diff <tiedosto>` | Näyttää muutokset verrattuna viimeiseen commitin versioon. |
| `git rm <tiedosto>` | Poistaa tiedoston työtilasta ja versionhallinnasta. |
| `git mv <vanha> <uusi>` | Nimeää tiedoston uudelleen tai siirtää hakemistoon. |
| `git reset <tiedosto>` | Poistaa tiedoston seuraavasta talletuksesta (staging). |
| `git restore <tiedosto>` | Palauttaa tiedoston viimeisimpään talletukseen, työtilamuutokset häviävät. |
| `git revert <commit>` | Luo uuden talletuksen, joka peruuttaa annetun commitin muutokset. |
| `git branch <nimi>` | Luo uuden haaran. |
| `git branch` | Näyttää olemassa olevat haarat. |
| `git switch <haara>` | Vaihtaa toiseen haaraan. |
| `git switch -c <haara>` | Luo uuden haaran ja vaihtaa siihen. |
| `git merge <haara>` | Yhdistää annetun haaran muutokset nykyiseen haaraan. |