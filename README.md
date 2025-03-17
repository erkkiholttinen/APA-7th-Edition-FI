# APA 7th Edition (FI) for Microsoft Word

Kunnes (ellei) Microsoft lisää mallin uusimmalle versiolle, tämä on alunperin Mike Slaglen ja Brian Kavanaugh'n muokkaama APA 7th Edition XSLT.

**TÄREKÄÄ**: Nämä tiedostot tarjotaan kohteliaisuutena niille, jotka tarvitsevat paremman vaihtoehdon APA 7:lle kuin mitä Microsoft tällä hetkellä tarjoaa suomen kieltä käytettäessä. En luonut mallia, vain muokkasin sitä hieman. Jos on ongelmia, voit koittaa tehdä tarvittavat muutokset (jos mahdollista; on olemassa rajoituksia sille, mitä voidaan tehdä) jonka jälkeen lähetä pull-pyyntö, jotta korjaukset saadaan jakoon muillekin.

## How to Use

Asennuksen jälkeen valitse Wordin viittaustyyliluettelosta APA7 FI -vaihtoehto.

Jotta kappaleviittaus saadaan luotua oikein niin että piste on sulkeiden sisällä, lisää viittauksen sivujen eteen teksti "kpl" (ilman lainausmerkkejä) (toissijainen hiiren painike viittauksessa ja valitse "Muokkaa viittausta"). Tämä aiheuttaa sen, että viittaus kirjoitetaan muodossa (KirjoittajanNimi, Vuosi.) sen sijaan, että se olisi (KirjoittajanNimi, Vuosi).

## Asennus

### Windows

#### Manuaalinen tapa
1. Sulje Word
2. Käytä Windows Explorer työkalua, kopioi tiedosto APASeventhEditionFI.xsl kansioon C:\Users\<your_user_name>\AppData\Roaming\Microsoft\Bibliography\Style 
3. Käynnistä Word. Lähdeviittauksissa tulisi nyt olla tyyli APA7 FI.
   
#### Asennus Bat tiedoston avulla
1. Sulje word
2. Kopioi APASeventhEditionFI.bat tiedosto ja tarvittaessa muokkaa tiedoston asetuksia, jotta voit ajaa sen.
3. Aja APASeventhEditionFI.bat tiedosto.
4. Käynnistä Word. Lähdeviittauksissa tulisi nyt olla tyyli APA7 FI.

Huomio: Bat tiedosto ajaa yksinkertaisesti seuraavan komennon:
```
curl https://raw.githubusercontent.com/erkkiholttinen/APA-7th-Edition-FI/main/APASeventhEditionFI.xsl -o "%appdata%\Microsoft\Bibliography\Style\APASeventhEditionFI.xsl"
```



### MacOS

#### Manuaalinen tapa
1. Sulje Word
2. Käytä Finder työkalua ja kopioi tiedosto APASeventhEditionFI.xsl seuraaviin kasnioihin:
    1. HD/Applications/Microsoft Word.app/Contents/Resources/Style/
    2. HD/Users/\<your_user_name>/Library/Containers/com.microsoft.Word/Data/Library/Application Support/Microsoft/Office/Style/
2. Käynnistä Word. Lähdeviittauksissa tulisi nyt olla tyyli APA7 FI. 

#### Asennus Shell scriptin avulla
* __Tiedosto pyyttää sudo oikeuksia. Aja tiedostoja sudo oikeuksilla vain jos varmasti ymmärrät mitä olet tekemässä.__
1. Sulje Word
2. Kopioi APASeventhEditionFI.sh tiedosto lokaaliin kansioon
3. Avaa Terminal applikaatio
4. Navigoi kansioon, jonne kopioit APASeventhEditionFI.sh tiedoston
    1. `cd /path/to/your/file`
5. Aja sh tiedosto
    1. `bash APASeventhEditionFI.sh`
    2. Kysyttäessä anna salasana sudo käskyä varten
    3. Tiedostojen tulisi kopioitua tarvittaviin paikkoin
6. Käynnistä Word. Lähdeviittauksissa tulisi nyt olla tyyli APA7 FI.
   
Huomioita:  
* Bash scripti käyttää curl käskyä, jolla se hakee trvittavat tiedostot githubista ja sijoittaa ne paikalliseen kansioon.
* Bash scripti tarkistaa, että tiedosto on kopioitunut ensimmäiseen kansioon oikein ja vasta tämän jälkeen tiedosto kopioidaan seuraavaan kansioon.


## Vastuuvapauslauseke

(sama kuin Mike'n ja Brian'n) Tarjoan tätä tiedostoa ja sen tarvittavaa sijaintia vain koulutustarkoituksiin. Jos MS Office -asennukset vahingoittuvat tämän tiedoston käytön seurauksena, en ole vastuussa ongelmien korjaamisesta tai korjaamisesta.
