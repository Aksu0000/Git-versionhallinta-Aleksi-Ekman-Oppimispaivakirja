# Oppimispäiväkirja: Git projektissa

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