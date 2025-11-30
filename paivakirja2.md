# Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Osion tehtävässä helpointa oli ymmärtää Gitin perustoimintoja, joita käsiteltiin edellisissä tehtävissä sekä luoda uusi tyhjä repositorio GitHubiin.

Haastavinta oli haarojen ja etärepositorion käsittely, erityisesti fetchin ja pullin erot ja merge-konfliktien hallinta.

Oppimisessa auttoi se, että tein käytännön harjoituksia Git-komentojen avulla ja vertasin eri komentojen vaikutuksia työtilaan. Myös ohjeistuksien selkeydestä oli paljon apua.

Esteet, kuten konfliktien syntyminen, selvitin käyttämällä `git status` ja `git log` -komentoja sekä tarkastelemalla dokumentaatiota.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
|---------|--------|
| `git remote add origin <url>` | Lisää uuden etärepositorion nimellä origin |
| `git remote` | Listaa määritellyt etärepositoriot |
| `git remote -v` | Listaa etärepositoriot ja niiden URL-osoitteet |
| `git fetch origin` | Hakee etärepositorion tiedot paikalliseen repositorioon, ei yhdistä |
| `git branch -r` | Listaa etärepositorion haarat |
| `git checkout main` | Vaihtaa paikalliseen master-haaraan |
| `git merge origin/main` | Yhdistää etärepositorion master-haaran paikalliseen master-haaraan |
| `git pull origin` | Hakee ja yhdistää muutokset etärepositorion nykyiseen haaraan |
| `git push origin main` | Vie paikallisen master-haaran etärepositorioon origin |
| `git push --all` | Vie kaikki paikalliset haarat etärepositorioon origin |
| `git push -u origin main` | Asettaa paikallisen master-haaran oletusarvoiseksi etähaaraan originissa |
| `git checkout origin/main` | Tutkii etärepositorion haaran sisältöä ilman yhdistämistä |
