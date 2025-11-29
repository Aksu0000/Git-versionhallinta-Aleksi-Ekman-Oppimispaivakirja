# Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Tehtävän helpoin osuus oli lisätä tyhjä repositorio GitHub palveluun sekä hyödyntää edellisessä vaiheessa läpokäytyjä Gitin perustoimintoja. Haarojen ja etärepositorion käsittely, erityisesti fetchin ja pullin erot ja merge-konfliktien hallinta osoittautui haastavaksi ymmärtää. Käytännön harjoitukset Git-komentojen avulla auttoivat oppimaan samalla tavalla kuin viime tehtävässä. Vertasin myös eri komentojen vaikutuksia työtilaan. Esteet selvitin käyttämällä `git status` ja `git log`-komentoja sekä tarkastelemalla dokumentaatiota ja kysymällä tekoälyltä apua kaikkein kiperimmissä tilanteissa. Näiden yhdistelmällä sain tehtävät tehtyä.


## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
|---------|--------|
| `git remote add origin <url>` | Lisää uuden etärepositorion nimellä origin |
| `git remote` | Listaa määritellyt etärepositoriot |
| `git remote -v` | Listaa etärepositoriot ja niiden URL-osoitteet |
| `git fetch origin` | Hakee etärepositorion tiedot paikalliseen repositorioon, ei yhdistä |
| `git branch -r` | Listaa etärepositorion haarat |
| `git checkout main` | Vaihtaa paikalliseen master-haaraan |
| `git merge origin/master` | Yhdistää etärepositorion master-haaran paikalliseen master-haaraan |
| `git pull origin` | Hakee ja yhdistää muutokset etärepositorion nykyiseen haaraan |
| `git push origin master` | Vie paikallisen master-haaran etärepositorioon origin |
| `git push --all` | Vie kaikki paikalliset haarat etärepositorioon origin |
| `git push -u origin master` | Asettaa paikallisen master-haaran oletusarvoiseksi etähaaraan originissa |
| `git checkout origin/master` | Tutkii etärepositorion haaran sisältöä ilman yhdistämistä |