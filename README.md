# Git-versionhallinta - git-oppimispäiväkirja

Tämä on kurssin oppimispäiväkirja.

**Kurssi:** Git-versionhallinta - SOF013AS2A-3001 
**Tekijä:** Aleksi Ekman  

## Kuvaus
Tämä repositorio sisältää oppimispäiväkirjan harjoituksista, jotka on tehty kurssin eri osioissa.  

## Oppimispäiväkirjan sisältö
Oppimispäiväkirjat on yhdistetty oletushaaraan `main`.  

# Oppimispäiväkirja kokonaisuudessaan:

## Oppimispäiväkirja: Paikallinen git
- [Päiväkirja 1](https://github.com/Aksu0000/Git-versionhallinta-Aleksi-Ekman-Oppimispaivakirja/blob/main/paivakirja1.md)

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Aluksi Gitin komennot ja eri tilojen (untracked, staged, modified) käsitteleminen tuntui jokseenkin sekavalta. Oli vaikeaa hahmottaa, miten tiedostot siirtyvät vaiheesta toiseen ja milloin muutokset todella tallentuvat versiohistoriaan. Myös projektien seuraaminen terminaalissa tuntui haastavalta, kun muutokset eivät tule suoraan näkyviin vaan ne pitää hakea esiin eri komennoilla. 

Uusien tiedostojen lisääminen repositorioon ja commitin tekeminen, kun perusajatus add- ja commit-vaiheista selkeni oli helpohkoa. Myös haarojen luominen ja vaihtaminen oli selkeää komentoja kokeilemalla.

Oppimista auttoi eniten käytännön harjoittelu. Kokeilin komentoja monta kertaa ja  katsoin `git status`-tuloksia useasti. Mahdolliset virheet ja niiden korjaaminen (reset, restore) auttoivat ymmärtämään Gitin logiikkaa.  

Esteitä selvitin lukemalla komennon tulosteen huolellisesti ja kokeilemalla varovaisesti erilaisia vaihtoehtoja. Erityisesti haarautumisen ja merge-konfliktien käsittely selkeytyi kokeilemalla erillisiä testihaaroissa. Lisäksi katsoin vinkkejä Youtubesta.


### Osiossa käyttämäni Git-komennot

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


## Oppimispäiväkirja: Hajautettu git
- [Päiväkirja 2](https://github.com/Aksu0000/Git-versionhallinta-Aleksi-Ekman-Oppimispaivakirja/blob/main/paivakirja2.md)

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Osion tehtävässä helpointa oli ymmärtää Gitin perustoimintoja, joita käsiteltiin edellisissä tehtävissä sekä luoda uusi tyhjä repositorio GitHubiin.

Haastavinta oli haarojen ja etärepositorion käsittely, erityisesti fetchin ja pullin erot ja merge-konfliktien hallinta.

Oppimisessa auttoi se, että tein käytännön harjoituksia Git-komentojen avulla ja vertasin eri komentojen vaikutuksia työtilaan. Myös ohjeistuksien selkeydestä oli paljon apua.

Esteet, kuten konfliktien syntyminen, selvitin käyttämällä `git status` ja `git log` -komentoja sekä tarkastelemalla dokumentaatiota.

### Osiossa käyttämäni Git-komennot

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


## Oppimispäiväkirja: Git projektissa
- [Päiväkirja 3](https://github.com/Aksu0000/Git-versionhallinta-Aleksi-Ekman-Oppimispaivakirja/blob/main/paivakirja3.md)

__Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?__

Versionhallinta helpottaa oman työn hallintaa, vaikka kehittäisin projektia yksin. Se avulla saadaan selkeä historia projektin kehityksestä. Selkeän versiohistorian avulla on helpompaa palata aikaisempaan versioon, jos jokin muutos ei toimikaan odotetusti. Versionhallinnan avulla on myös mahdollista tehdä turvallisesti kokeiluja eri haaroissa ilman, että pääversio vaarantuu. Versionhallinta myös dokumentoi muutokset automaattisesti, mikä tekee projektin ylläpidosta ja jatkokehityksestä sujuvampaa.

__Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?__

Monen kehittäjän projektissa versionhallinta vaikuttaisi olevan lähes välttämätön työkalu. Se mahdollistaa samanaikaisen työskentelyn eri ominaisuuksien parissa, auttaa seuraamaan, kuka teki mitäkin muutoksia, ja varmistaa, että kaikki käyttävät viimeisintä versiota koodista. Lisäksi versionhallinta helpottaa konfliktien havaitsemista ja ratkaisemista ja todennäköisesti parantaa koko tiimin yhteistyötä.

__Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.__

1. **Käytetään keskitettyä mallia**: Kaikilla tiimin jäsenillä on oma paikallinen kopio yhteisestä etärepositoriosta.  
2. **Haarat**: Master/päähaaraa käytetään vain valmiille, testatuille versioille. Ominaisuuksille ja kehitysprojekteille tehdään omat haarat.  
3. **Työnkulku**:
   - Kloonaa yhteinen repositorio:  
     ```bash
     git clone <repositorio-url>
     ```
   - Luo develop-haara uusille ominaisuuksille ja vaihda siihen:  
     ```bash
     git switch -c develop
     ```
   - Tee muutokset paikallisesti ja tallenna ne:  
     ```bash
     git add .
     git commit -m "Kuvaava viesti muutoksesta"
     ```
   - Hae muiden tekemät muutokset ja yhdistä ne omaan työhösi:  
     ```bash
     git fetch origin
     git merge origin/develop
     ```
     tai käytä yhdistelmäkomentoa:
     ```bash
     git pull origin develop
     ```
   - Ratkaise mahdolliset konfliktit ja vie valmiit muutokset etärepositorioon:  
     ```bash
     git push origin develop
     ```
4. **Yhdistämispyynnöt (pull request)**:  
   - Ominaisuushaarojen muutokset yhdistetään päähaaraan yhdistämispyynnön kautta, jotta tiimin jäsenet voivat kommentoida ja tarkistella koodia ennen varsinaista muutosta.  
   - Yhdistämispyynnöt dokumentoivat muutokset.
5. **Commit-viestien käytännöt**:
   - Ensimmäinen rivi max 50 merkkiä, kuvaa muutoksen lyhyesti.  
   - Tarvittaessa tarkempi kuvaus rivinvaihdolla erotettuna.  
   - Tee loogisista kokonaisuuksista erilliset commitit.

__Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?__

Opintojakson sisältö ja harjoitukset Gitin käytöstä olivat erittäin hyödyllisiä. Materiaalit ovat selkeitä ja harjoitukset tukivat hyvin oppimista käytännön tasolla. Erityisesti harjoitukset, joissa tehiin yhdistämispyyntö ja ratkaistiin konflikteja, auttoivat ymmärtämään, miten oikea tiimityö versionhallinnassa todennäköisesti toimii. Työmäärä oli sopiva kahden opintopisteen kurssiksi.
