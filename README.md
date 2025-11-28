# Soveltava Matematiikka ja fysiikka ohjelmoinnissa

## 📊 Python — PhyPhox Data-analyysi

**Tekijä:** Sara Vehviläinen  
**Oppilaitos:** Oulun ammattikorkeakoulu  
**Kurssi:** Soveltava matematiikka ja fysiikka ohjelmoinnissa  
**Lukukausi:** Syksy 2025

---

### 🧩 Projektien kuvaus
Tämä repositorio sisältää neljä fysiikan mittausdatan analyysiprojektia:

1. **Fysiikka1:** Kiihtyvyysanalyysi (liikuttelu)
2. **Fysiikka2:** Askelmittari (kävelyanalyysi)
3. **Fysiikka3:** GPS-reitin analyysi (paikannus ja matkan laskenta)
4. **Fysiikka4:** Signaalinanalyysi (FFT ja tehospektri)

Kaikki tehtävät analysoidaan Python-ohjelmilla ja ovat osa Soveltava matematiikka ja fysiikka -kurssia.

---

## 🎯 FYSIIKKA1: Kiihtyvyysanalyysi

### 📐 Analyysiperusteet
- **Mittausaika:** 19.7 sekuntia
- **Datapisteitä:** 1975 kpl (~100 Hz näytteenottotaajuus)
- **Komponentit:** 
  - X-komponentti (sivuttaissuunta)
  - Y-komponentti (pystysuunta) 
  - Z-komponentti (syvyyssuunta)
- **Absoluuttinen kiihtyvyys:** √(x² + y² + z²)

### ✨ Toiminnallisuus
- PhyPhox-datan lukeminen CSV-muodosta
- Kiihtyvyyskomponenttien visualisointi matplotlib-kirjastolla
- Automaattinen Word-dokumentin luonti kaikilla kuvaajilla
- Erillisten PNG-kuvaajien tallennus jokaiselle komponentille
- Puhelimen ruutukaapauden yhdistäminen analyysiin

---

## 🚶 FYSIIKKA2: Askelmittari

### 📐 Analyysiperusteet
- **Mittaustyyppi:** Kävelyanalyysi PhyPhox-kiihtyvyysdatasta
- **Menetelmät:** 
  - Tehospektrianalyysi (askeltaajuuden löytäminen)
  - Band-pass suodatus (hälyn poisto)
  - Askeleiden tunnistus (huiput + nollakohtien ylitykset)
- **Automaattiset toiminnot:**
  - Sarakkeiden tunnistus CSV:stä
  - Parhaan signaalin valinta
  - Kuvaajien tallennus PNG-muotoon

### ✨ Toiminnallisuus
- Automaattinen CSV-datan lukeminen ja sarakkeiden tunnistus
- Askeltaajuuden löytäminen tehospektrianalyysilla
- Signaalin suodatus band-pass-menetelmällä
- Askelten laskenta kahdella menetelmällä (vertailu)
- Automaattinen raportointi ja kuvaajien tallennus

---

## 🗺️ FYSIIKKA3: GPS-reitin analyysi

### 📐 Analyysiperusteet
- **Mittaustyyppi:** GPS-paikannus PhyPhox-sovelluksella
- **Kuljettu matka:** ~0.632 km (Haversinen kaava)
- **Menetelmät:**
  - Interaktiivinen karttavisualisointi (Folium)
  - Haversinen kaava matkan laskentaan
  - GPS-tarkkuuden ja satelliittien analyysi
- **Tehtävän osat:**
  - a) Reitin piirtäminen kartalle
  - b) Mittauksen luotettavuuden arviointi
  - c) Satelliittien ja tarkkuuden visualisointi
  - d) Matkan laskenta Haversinen kaavalla

### ✨ Toiminnallisuus
- Interaktiivinen HTML-kartta Folium-kirjastolla
- GPS-tarkkuuden värikoodaus kartalla (vihreä/oranssi/punainen)
- Satelliittien määrän ja tarkkuuden kuvaajat
- Matkan laskenta maapallon kaarevuus huomioiden
- Automaattinen kuvaajien tallennus PNG-muotoon

---

## 🔊 FYSIIKKA4: Signaalinanalyysi

### 📐 Analyysiperusteet
- **Mittaustyyppi:** Digitaalisen signaalin taajuusanalyysi
- **Menetelmät:**
  - FFT (Fast Fourier Transform) - Nopea Fourier-muunnos
  - Tehospektrianalyysi (Power Spectral Density)
  - Taajuuskomponenttien tunnistus
- **Parametrit:**
  - Näytteenottotaajuus: 1000 Hz
  - Teho desibeleinä (dB-asteikko)
  - Taajuusalue: 0 - 500 Hz (Nyquistin taajuus)

### ✨ Toiminnallisuus
- Excel-datan lukeminen ja esikäsittely
- FFT-muunnos aikatasosta taajuustasoon
- Tehospektrin laskenta ja visualisointi
- Dominoivan taajuuden automaattinen tunnistus
- Kuvaajien tallennus PNG-muotoon (300 dpi)
- Selkeä konsolituloste analyysin tuloksista

---

## 🛠️ Käytetyt teknologiat ja kirjastot
- **Python 3**
- **Pandas** - Datan käsittely ja analyysi
- **Matplotlib** - Kuvaajien piirtäminen ja visualisointi
- **NumPy** - Numeerinen laskenta ja FFT-muunnokset
- **SciPy** - Signaalien käsittely (askelmittari)
- **Folium** - Interaktiiviset kartat (GPS-analyysi)
- **python-docx** - Word-dokumenttien automaattinen luonti
- **OpenPyXL** - Excel-tiedostojen lukeminen
- **PhyPhox** - Mittausdatan keräys älypuhelimella

---

## 📁 Projektirakenne

```plaintext
Soveltava_fysiikka/
├── README.md                          # Projektien dokumentaatio
├── Fysiikka1/                         # Kiihtyvyysanalyysi
│   ├── datan_kuvajaa.ipynb           # Python-analyysi (Jupyter Notebook)
│   ├── kiihtyvyys.csv                # PhyPhox mittausdata
│   ├── Kiihtyvyys_kuva.jpg          # Puhelimen ruutukaappaus
│   ├── Tehtava1_palautus_Sara_Vehvilainen.docx  # Lopullinen palautus
│   ├── Tehtava1_palautus_Sara_Vehvilainen.pdf   # PDF-versio
│   ├── kuvaajat/                     # Erilliset PNG-kuvaajat
│   │   ├── 01_yhdistetty.png        
│   │   ├── 02_x_komponentti.png     
│   │   ├── 03_y_komponentti.png     
│   │   └── 04_z_komponentti.png     
│   └── meta/                         # PhyPhox metadata
│       ├── device.csv               
│       └── time.csv                
├── Fysiikka2/                         # Askelmittari
│   ├── askelmittari.ipynb            # Python askelmittari-analyysi (ensimmäinen versio)
│   ├── Tehtava2_askelmittari.ipynb   # Päivitetty versio
│   ├── walk.csv                      # PhyPhox kävelymittausdata
│   ├── Askelmittari_kuva.png         # Puhelimen ruutukaappaus
│   ├── Tehtava2eka_Askelmittari_Palautus_Sara_Vehvilainen.docx  # Ensimmäinen palautus
│   ├── Tehtava2eka_Askelmittari_Palautus_Sara_Vehvilainen.pdf   # PDF-versio
│   ├── Tehtava2_Askelmittari_Palautus_Sara_Vehvilainen.docx     # Lopullinen palautus
│   ├── Tehtava2_Askelmittari_Palautus_Sara_Vehvilainen.pdf      # PDF-versio
│   ├── 01_alkuperaiset_mittaukset.png # Automaattisesti luodut kuvaajat
│   ├── 01_raakadata.png              
│   ├── 02_tehospektrit.png           
│   ├── 03_suodatus.png               
│   ├── 04_askeleiden_tunnistus.png   
│   ├── Tehtava2/                     # Tyhjä kansio
│   └── meta/                         # PhyPhox metadata
│       ├── device.csv               
│       └── time.csv 
├── Fysiikka3/                         # GPS-reitin analyysi
│   ├── kartta.ipynb                  # Python GPS-analyysi
│   ├── GPS.csv                       # PhyPhox GPS-mittausdata
│   ├── reitti_phyphox.html          # Interaktiivinen kartta
│   ├── Kavelyreitti.jpg             # Reitin valokuva
│   ├── phyphox-kartta.png           # PhyPhox-sovelluksen karttanäkymä
│   ├── gps_kuvaajat.png             # Yhdistetty kuvaaja
│   ├── satelliitit_aika.png         # Satelliittien määrä ajassa
│   ├── tarkkuus_aika.png            # GPS-tarkkuus ajassa
│   ├── satelliitit_jakauma.png      # Satelliittien jakauma
│   ├── tarkkuus_jakauma.png         # Tarkkuuden jakauma
│   ├── tarkkuus_kuvaaja.png         # Tarkkuuden yksityiskohtainen kuvaaja
│   ├── Tehtava3_Palautus_ Sara_Vehvilainen.docx  # Palautus (huom. välilyönti)
│   ├── Tehtava3_Palautus_ Sara_Vehvilainen.pdf   # PDF-versio
│   └── meta/                         # PhyPhox metadata
│       ├── device.csv               
│       └── time.csv                 
└── Fysiikka4/                         # Signaalinanalyysi
    ├── Signaali.ipynb                # Python FFT-analyysi
    ├── Signaali.xlsx                 # Mittausdata (Excel)
    ├── aikasignaali.png              # Aikatasokuvaaja
    ├── tehospektri.png               # Taajuustasokuvaaja
    ├── Python_koodi1.png             # Koodikuvat dokumentaatioon
    ├── Python_koodi2.png             
    ├── Python_koodi3.png             
    └── Tehtava3_Palautus_Sara_Vehvilainen.docx  # Palautus
```

### 🎯 Oppimistavoitteet
#### Fysiikka1:
- PhyPhox-mittausdatan keräys ja käsittely
- Python-datan-analyysi pandas-kirjastolla
- Tieteellisten kuvaajien luominen matplotlib-kirjastolla
- Automaattinen raportointi python-docx-kirjastolla
- Kiihtyvyyskomponenttien ymmärtäminen fysikaalisesti

#### Fysiikka2:
- Signaalien käsittely ja suodatus (SciPy)
- Tehospektrianalyysi ja taajuustarkastelu
- Automaattiset algoritmit (huippujen ja nollakohtien tunnistus)
- Fysikaaliset mittausmenetelmät (askelmittari)
- Kahden menetelmän vertailu ja validointi

#### Fysiikka3:
- GPS-paikannuksen perusteet ja tarkkuus
- Haversinen kaavan soveltaminen matkan laskentaan
- Interaktiivisten karttojen luonti (Folium)
- Satelliittien vaikutus GPS-tarkkuuteen
- Mittausdatan luotettavuuden arviointi

#### Fysiikka4:
- Fourier-muunnoksen teoria ja sovellukset
- FFT-algoritmin käyttö taajuusanalyysissä
- Tehospektrin tulkinta ja dominoivien taajuuksien tunnistus
- Nyquistin teoreema ja näytteenottotaajuus
- Aikatasosta taajuustasoon siirtyminen
- Logaritminen dB-asteikko signaalitehon esittämisessä

---

### 📝 Huomioita
#### Fysiikka1:
- PhyPhox tallentaa datan tieteellisessä notaatiossa (E-notaatio)
- Aika mitataan sekunteina mittauksen alusta
- Kiihtyvyys mitataan m/s² -yksikössä
- Absoluuttinen kiihtyvyys lasketaan automaattisesti PhyPhoxissa

#### Fysiikka2:
- Askelmittari käyttää signaalin suodatusta hälyn poistoon
- Kaksi laskumenetelmää antaa vertailukelpoisia tuloksia
- Automaattinen sarakkeiden tunnistus toimii eri PhyPhox-versioilla
- Kuvaajat tallennetaan automaattisesti PNG-muotoon

#### Fysiikka3:
- GPS-tarkkuus vaihtelee satelliittien määrän mukaan
- Haversinen kaava ottaa huomioon maapallon kaarevuuden
- Interaktiivinen kartta voidaan avata selaimessa (HTML)
- Värikoodaus helpottaa tarkkuuden arviointia
- Kuljettu matka: noin 0.632 km, keskinopeus: 5.69 km/h (kävelynopeus)

#### Fysiikka4:
- FFT on tehokas algoritmi Fourier-muunnoksen laskemiseen
- Näytteenottotaajuuden on oltava vähintään 2× signaalin maksimitaajuus (Nyquist)
- Tehospektri paljastaa signaalin taajuuskomponentit
- dB-asteikko (10·log₁₀(P)) sopii laajan dynamiikan esittämiseen
- Excel-data voidaan lukea suoraan pandas-kirjastolla

---

## 📚 Oppimisresurssit

### Python ja Data Science:
- [Pandas Documentation](https://pandas.pydata.org/docs/) - Datan käsittelyn perusteet
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html) - Kuvaajien piirtäminen
- [NumPy Documentation](https://numpy.org/doc/) - Numeerinen laskenta
- [SciPy Documentation](https://scipy.org/doc/) - Signaalien käsittely ja tieteellinen laskenta
- [Folium Documentation](https://python-visualization.github.io/folium/) - Interaktiiviset kartat
- [Python-docx Documentation](https://python-docx.readthedocs.io/) - Word-dokumenttien luonti

### PhyPhox ja fysiikka:
- [PhyPhox Website](https://phyphox.org/) - Virallinen PhyPhox-sivusto
- [PhyPhox Documentation](https://phyphox.org/wiki/) - PhyPhox-dokumentaatio
- [Accelerometer Physics](https://en.wikipedia.org/wiki/Accelerometer) - Kiihtyvyysantureiden fysiikka
- [Haversine Formula](https://en.wikipedia.org/wiki/Haversine_formula) - Matkan laskenta pallon pinnalla
- [GPS Accuracy Factors](https://en.wikipedia.org/wiki/Error_analysis_for_the_Global_Positioning_System) - GPS-tarkkuuteen vaikuttavat tekijät

### Jupyter Notebook:
- [Jupyter Documentation](https://jupyter.org/documentation) - Jupyter Notebook -dokumentaatio
- [JupyterLab Documentation](https://jupyterlab.readthedocs.io/) - JupyterLab-käyttöliittymä

### Työkalut ja ympäristöt:
- [Anaconda Distribution](https://www.anaconda.com/) - Python-tiedepaketti
- [VS Code Python Tools](https://code.visualstudio.com/docs/python/python-tutorial) - Python-kehitystyökalut
- [Google Colab](https://colab.research.google.com/) - Pilvi-Jupyter Notebook
