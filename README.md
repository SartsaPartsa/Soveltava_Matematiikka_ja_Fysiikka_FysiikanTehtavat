# Soveltava Matematiikka ja fysiikka ohjelmoinnissa

## 📊 Python — PhyPhox Kiihtyvyysanalyysi

**Tekijä:** Sara Vehviläinen  
**Oppilaitos:** Oulun ammattikorkeakoulu  
**Kurssi:** Soveltava matematiikka ja fysiikka  
**Lukukausi:** Syksy 2025

### 🧩 Tehtävän kuvaus
Tämä projekti analysoi PhyPhox-sovelluksella kerättyä kiihtyvyysdataa Python-ohjelmalla. Mittauksessa liikutettiin puhelinta eri suuntiin ~20 sekunnin ajan ja analysoitiin tulokset kolmessa koordinaattisuunnassa (x, y, z).

Tehtävä on osa Soveltava matematiikka ja fysiikka -kurssia.

### 📐 Analyysiperusteet
- **Mittausaika:** 19.7 sekuntia
- **Datapisteitä:** 1975 kpl (~100 Hz näytteenottotaajuus)
- **Komponentit:** 
  - X-komponentti (sivuttaissuunta)
  - Y-komponentti (pystysuunta) 
  - Z-komponentti (syvyyssuunta)
- **Absoluuttinen kiihtyvyys:** √(x² + y² + z²)

## ✨ Toiminnallisuus
- PhyPhox-datan lukeminen CSV-muodosta
- Kiihtyvyyskomponenttien visualisointi matplotlib-kirjastolla
- Automaattinen Word-dokumentin luonti kaikilla kuvaajilla
- Erillisten PNG-kuvaajien tallennus jokaiselle komponentille
- Puhelimen ruutukaapauden yhdistäminen analyysiin

## 🛠️ Käytetyt teknologiat ja kirjastot
- **Python 3**
- **Pandas** - Datan käsittely ja analyysi
- **Matplotlib** - Kuvaajien piirtäminen ja visualisointi
- **NumPy** - Numeerinen laskenta
- **python-docx** - Word-dokumenttien automaattinen luonti
- **PhyPhox** - Mittausdatan keräys älypuhelimella


## 📊 Analyysin suorittaminen
1. **Solu 1:** Lataa PhyPhox CSV-data ja näytä ensimmäiset rivit
2. **Solu 2:** Piirrä peruskuvaaja kaikille komponenteille
3. **Solu 3:** Luo automaattisesti Word-dokumentti kaikilla kuvaajilla

## 📁 Projektikansio
```plaintext

Fysiikka1/
├── README.md                           # Projektin dokumentaatio
├── datan_kuvajaa.ipynb                # Python-analyysi (Jupyter Notebook)
├── Raw Data.csv                       # PhyPhox mittausdata
├── Kiihtyvyys_kuva.jpg               # Puhelimen ruutukaappaus
├── Tehtava1_palautus_Sara_Vehvilainen.docx  # Lopullinen palautus
├── Tehtava1_palautus_Sara_Vehvilainen.pdf   # PDF-versio
├── kuvaajat/                          # Erilliset PNG-kuvaajat
│   ├── 01_yhdistetty.png             # Kaikki komponentit yhdessä
│   ├── 02_x_komponentti.png          # X-komponentti erikseen
│   ├── 03_y_komponentti.png          # Y-komponentti erikseen
│   └── 04_z_komponentti.png          # Z-komponentti erikseen
└── meta/                              # PhyPhox metadata
    ├── device.csv                     # Laitetiedot ja anturitiedot
    └── time.csv                       # Aikaleimoja ja synkronointitiedot
```

### 🎯 Oppimistavoitteet
- PhyPhox-mittausdatan keräys ja käsittely
- Python-datan-analyysi pandas-kirjastolla
- Tieteellisten kuvaajien luominen matplotlib-kirjastolla
- Automaattinen raportointi python-docx-kirjastolla
- Kiihtyvyyskomponenttien ymmärtäminen fysikaalisesti
- CSV-datan lukeminen ja käsittely Pythonilla

### 📝 Huomioita
- PhyPhox tallentaa datan tieteellisessä notaatiossa (E-notaatio)
- Aika mitataan sekunteina mittauksen alusta
- Kiihtyvyys mitataan m/s² -yksikössä
- Absoluuttinen kiihtyvyys lasketaan automaattisesti PhyPhoxissa
- Word-dokumentti luodaan automaattisesti väliaikaisten PNG-tiedostojen kautta

## 📚 Oppimisresurssit

### Python ja Data Science:
- [Pandas Documentation](https://pandas.pydata.org/docs/) - Datan käsittelyn perusteet
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html) - Kuvaajien piirtäminen
- [NumPy Documentation](https://numpy.org/doc/) - Numeerinen laskenta
- [Python-docx Documentation](https://python-docx.readthedocs.io/) - Word-dokumenttien luonti

### PhyPhox ja fysiikka:
- [PhyPhox Website](https://phyphox.org/) - Virallinen PhyPhox-sivusto
- [PhyPhox Documentation](https://phyphox.org/wiki/) - PhyPhox-dokumentaatio
- [Accelerometer Physics](https://en.wikipedia.org/wiki/Accelerometer) - Kiihtyvyysantureiden fysiikka

### Jupyter Notebook:
- [Jupyter Documentation](https://jupyter.org/documentation) - Jupyter Notebook -dokumentaatio
- [JupyterLab Documentation](https://jupyterlab.readthedocs.io/) - JupyterLab-käyttöliittymä

### Työkalut ja ympäristöt:
- [Anaconda Distribution](https://www.anaconda.com/) - Python-tiedepaketti
- [VS Code Python Tools](https://code.visualstudio.com/docs/python/python-tutorial) - Python-kehitystyökalut
- [Google Colab](https://colab.research.google.com/) - Pilvi-Jupyter Notebook
