# 📱 PhyPhox Kiihtyvyysmittaus - Fysiikan Tehtävä 1

## 👤 Tekijä

**Sara Vehviläinen**  
Soveltava fysiikka - Fysiikka 1  

## 📅 Päivämäärä

Luotu: Marraskuu 2025

## 📋 Projektin kuvaus

Tämä projekti analysoi puhelimella mitattua kiihtyvyysdataa PhyPhox-sovelluksella. Tehtävässä tutkitaan puhelimen liikettä kolmessa suunnassa (x, y, z) ja luodaan visuaaliset kuvaajat Python-ohjelmalla.

## 📁 Tiedostorakenne

```plaintext
Fysiikka1/
├── datan_kuvajaa.ipynb          # Pääanalyysikoodi (Jupyter Notebook)
├── Raw Data.csv                 # PhyPhox-mittausdata (1975 datapistettä)
├── Kiihtyvyys_kuva.jpg         # Puhelimen ruutukaappaus mittauksen aikana
├── README.md                    # Tämä tiedosto
├── kuvaajat/                    # Generoitut kuvaajat
│   ├── 01_yhdistetty.png       # Kaikki komponentit yhdessä
│   ├── 02_x_komponentti.png    # X-suunnan kiihtyvyys
│   ├── 03_y_komponentti.png    # Y-suunnan kiihtyvyys
│   └── 04_z_komponentti.png    # Z-suunnan kiihtyvyys
├── meta/                        # Metadata-tiedostot
│   ├── device.csv              # Laitteen tiedot (iPhone 14 pro)
│   └── time.csv                # Aikaleimadata
├── Tehtava1_palautus_Sara_Vehvilainen.docx  # Word-palautus
└── Tehtava1_palautus_Sara_Vehvilainen.pdf   # PDF-palautus
```

## 🔬 Mittausdata

- **Mittauslaite:** iPhone 14 pro
- **Sovellus:** PhyPhox v1.2.0
- **Mittauksen kesto:** ~6.9 sekuntia
- **Datapisteitä:** 1975 kpl
- **Mittaustiheys:** ~285 Hz
- **Mitatut suureet:**
  - Aika (s)
  - Lineaarinen kiihtyvyys X-suunnassa (m/s²)
  - Lineaarinen kiihtyvyys Y-suunnassa (m/s²)
  - Lineaarinen kiihtyvyys Z-suunnassa (m/s²)
  - Kokonaiskiihtyvyys (m/s²)

## 🐍 Python-analyysi

### Käytetyt kirjastot:
- `pandas` - Datan käsittely
- `numpy` - Numeeriset laskut
- `matplotlib` - Kuvaajien piirtäminen
- `python-docx` - Word-dokumentin luonti

### Analyysin vaiheet:
1. **Datan lataus** - CSV-tiedoston lukeminen
2. **Visualisointi** - Kuvaajien luonti kaikille komponenteille
3. **Raportointi** - Automaattinen Word-dokumentin generointi

## 📊 Tulokset

Analyysi tuottaa seuraavat kuvaajat:

1. **Yhdistetty kuvaaja** - Kaikki kolme kiihtyvyyskomponenttia samassa kuvassa
2. **X-komponentti** - Sivuttaissuunnan kiihtyvyys (punainen)
3. **Y-komponentti** - Pystysuunnan kiihtyvyys (vihreä)
4. **Z-komponentti** - Syvyyssuunnan kiihtyvyys (sininen)

## 🚀 Käyttöohje

### Vaatimukset:
- Python 3.x
- Jupyter Notebook
- Tarvittavat kirjastot: pandas, numpy, matplotlib, python-docx

### Ajaminen:
1. Avaa `datan_kuvajaa.ipynb` Jupyter Notebookissa
2. Suorita kaikki solut järjestyksessä
3. Kuvaajat generoituvat automaattisesti `kuvaajat/` kansioon
4. Word-dokumentti luodaan automaattisesti palautusta varten

## 📈 Fysiikan tarkastelu

Mittaus näyttää puhelimen kiihtyvyysmuutokset kolmessa ulottuvuudessa:
- **X-akseli:** Sivuttaisliike (vasemmalle/oikealle)
- **Y-akseli:** Pystyliike (ylös/alas)
- **Z-akseli:** Eteen/taakse-liike

Data mahdollistaa puhelimen liikekuvion analysoimisen ja fysiikallisten suureiden tarkastelun.
