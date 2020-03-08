# UiPathVerkkokauppa

KÄYTTÖ:

1. Käynnistä sovellus.
2. Syötä halutut hakutiedot ja tiedostosijainti.
3. Ohjelma hakee täysin automaattisesti "https://www.verkkokauppa.com/" -sivustolta dataa, tallentaa ja suodattaa datan exel -tiedostoon.

TOIMINTALOGIIKKA:

1. Hakee käyttäjältä tiedot forms kyselyn avulla ja tallentaa ne muuttujiin.

2. Avaa selaimen osoitteessa "https://www.verkkokauppa.com/". Syöttää kyselyssä saadun tiedon hakukenttään ja painaa automaattisesti 
  "suurennuslasia". Selaimessa avautuu lista tuotteita.
  
3. Datan hakeminen tapahtuu "Data Scraping" työkalulla, joka tallentaa tiedot väliaikaiseen taulukkoon (datatable). Ohjelma osaa vaihtaa
  hakutuloksia selattaessa seuraavan sivun. Lisäksi For Each Row loopilla vaihdetaan saaduista hinnoista pilkut pisteiksi, jotta lukuja
  voidaan käsitellä desimaalilukuina.
  
4. Ohjelma luo uuden excel-taulukon kyselyssä annettuun sijaintiin ja nimeää tiedoston ""haettava tuotekategoria" + "Data.xlsx"". 

5. Ohjelma avaa juuri luodun excel-taulukon ja lajittelee tulokset forms kyselyssä annettujen rajoitteiden mukaan. Lisäksi ohjelma maalaa 
  halutut tulokset vihreiksi ja ei-halutut tulokset punertavaksi if-lauseen avulla. Samalla ohjelma kopioi hyväksytyt rivit helpommin 
  näkyville sarakkeisiin E ja F.
