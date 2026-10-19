# OT-Autopesut – nettisivu GitHub Pagesiin ja Velloon

Tämä on pelkkä staattinen nettisivu (`index.html` + `media`-kansio). Siinä ei ole omaa palvelinta eikä omaa varausjärjestelmää.

- **Ajanvaraus** hoidetaan Vellon varauskalenterilla, joka on upotettu sivulle (kohta "Varaa pesu"). Vellossa varataan vain aika.
- **Hinnat ja alennukset** näytetään pelkästään sivulla. Alennukset huomioidaan maksun yhteydessä paikan päällä.

## 1. Vellon asetukset

Ehdotus kalenteriin: aukioloajat 16.00–21.00 puolen tunnin välein, ei sunnuntaisin. Varauksessa kannattaa kysyä **osoite, jossa auto on**.

Sivulla on valmiina Vellon upotuskoodi:

    <script async src="https://static.vello.fi/embed/v1.js" data-url="ot-autopesut" data-lang="fi"></script>

Jos Vellon osoite (`ot-autopesut`) tai upotuskoodi muuttuu, etsi `index.html`:stä teksti `static.vello.fi` ja muuta se.

Tarkista Vellosta, että kalenteri näkyy julkaistulla sivulla (esikatselu ei sitä näytä) ja että saat ilmoituksen uusista varauksista.

## 2. Julkaise GitHub Pagesissa

1. Luo tili osoitteessa github.com.
2. Luo uusi repository (esim. `ot-autopesut`). GitHub Pages -sivusto on julkinen.
3. Lataa repositoryyn tiedostot: `index.html`, `.nojekyll` ja `media`-kansio (sisältöineen). "Add file → Upload files".
4. Asetukset: Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, kansio `/ (root)` → Save.
5. Hetken kuluttua sivu aukeaa GitHubin antamassa osoitteessa. Kokeile, että Vellon kalenteri latautuu.
6. Oma domain: osta ot-autopesut.com, kirjoita se kohtaan Settings → Pages → Custom domain ja lisää domainin DNS-asetuksiin GitHubin ohjeen mukaiset tietueet. Ota lopuksi käyttöön "Enforce HTTPS".

## 3. Muokkaaminen

Hinnat, tekstit ja värit ovat `index.html`:ssä. Muuta tiedostoa ja lataa se uudelleen GitHubiin, niin sivu päivittyy. Kuvat ja videot ovat `media`-kansiossa.

## Mitä tässä versiossa ei ole

- Omaa hallintanäkymää (käytät Vellon omaa hallintaa).
- Hinnanlaskentaa varauksen yhteydessä: hinnat ovat vain sivun tekstinä.
- Ensikertalaisuuden automaattista tarkistusta: tarkistat sen tarvittaessa käsin.
- Omia sähköposti-ilmoituksia (Vello hoitaa, jos tukee).

Maksu-, peruutus- ja tietosuojatekstit ovat sivun lopussa. Tietosuojaseloste on pohja, ja sitä pitää päivittää, kun tiedät, miten Vello käsittelee tietoja.
