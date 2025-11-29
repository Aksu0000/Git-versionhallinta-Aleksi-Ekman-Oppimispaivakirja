# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Aluksi Gitin komennot ja eri tilojen (untracked, staged, modified) käsitteleminen tuntui jotenkin sekavalta. Oli haastavaa hahmottaa, miten tiedostot siirtyvät vaiheesta toiseen ja milloin muutokset todella tallentuvat.  

Uusien tiedostojen lisääminen repositorioon ja commitin tekeminen oli helpohkoa, kun perusajatus add- ja commit-vaiheista selkeytyi materiaalien ja tehtävien myötä. Myös haarojen luominen ja vaihtaminen oli selkeää komentoja kokeilemalla.

Oppimista auttoi eniten käytännön harjoittelu. Kokeilin komentoja useaan kertaan, katsoin `git status`-tuloksia ja testasin `git checkout`- ja `git revert`-komentoja. Mahdolliset virheet ja niiden korjaaminen (reset, restore) auttoivat ymmärtämään Gitin logiikkaa.  

Esteet selvisivät usein lukemalla komennon tulosteen huolellisesti vertaamalla sitä materiaaleihin ja kokeilemalla varovaisesti erilaisia vaihtoehtoja. Sekä katsomalla vinkkejä mm. youtubesta.

---

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| `mkdir demo` | Luo tyhjän hakemiston nimellä demo. |
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
| `git clone <url>` | Kopioi olemassa olevan repositorion ja asettaa sen etärepositoriksi. |
