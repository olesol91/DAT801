# Konfigurer din datamaskin

Hvis du ønsker å bruke din egen maskin til å arbeide med kursmaterialet bør du følge disse instruksjonene. 

> NB: Som nevnt er dette valgfritt: du kan også bruke skytjenester til å arbeide med kodematerialet, for slik å unngå potensielle installasjonsproblemer.


## Allerede installert, og skal bare tilbake til arbeidet?
_Merk at du kun behøver å kjøre gjennom denne oppskriften én gang per maskin du ønsker å bruke. Hvis du har installert alt og bare skal starte opp Jupyter Notebook for å fortsette arbeidet, skriv følgende i din terminal (Anaconda Prompt hvis du bruker Windows) for å (i) gå inn i katalogen du har lagret kursrepositoriet, (ii) laste ned eventuelle oppdateringer, (iii) aktivere Python-omgivelsene og (iv) starte Jupyter Notebook. Hvis du har lagret dat801-repositoriet et annet sted på maskinen, må du bruke `cd` (som betyr «Change Directory») til du står inne i korrekt katalog._
```bash
cd dat801 
git pull && conda env update
conda activate dat801
jupyter notebook
``` 

## Mac-bruker?
Hvis du bruker MacOS må du først installere Xcode (gratis): https://developer.apple.com/xcode/resources/. Deretter:
1. Start `terminal.app` (søk med CMD+SPACE)
2. Skriv `xcode-select --install`



## GitHub
Kodematerialet hostes på kode-delingsplattformen GitHub (der du også leser dette). Opprett en brukerkonto via denne lenken: [https://github.com/join](https://github.com/join). 

## Kaggle
[Kaggle](https://www.kaggle.com) er et online felleskap for «data scientist» som arrangerer en rekke konkurranser og tilgjengeligjør mange datasett. Vi skal bruke Kaggle i DAT801, både for kursprosjekter og som kilde til datamaterialet. Opprett en konto her: [https://www.kaggle.com](https://www.kaggle.com).

## Anaconda

Python bør installeres via [Anaconda Distribution](https://www.anaconda.com/products/individual#Downloads).

Etter installasjon, kjør `python --version` i et terminal-vindu (på Windows, bruk «Anaconda Prompt»). Hvis output inneholder "Python" og "Anaconda" er du klar for neste steg.


## Installer og test kursets programvare-omgivelser

Etter installasjon av Anaconda, gå gjennom følgende steg. Bruk et terminalvindu på GNU/Linux og MacOS, "Anaconda Prompt" på Windows. 

### Installer Git

```bash
conda install git
```

### Last ned kursrepositoriet

```bash
git clone https://github.com/alu042/DAT801
cd DAT801
```

### Oppdater conda
```bash
conda update -n base -c defaults conda
```

### Konfigurer Python-omgivelsene
```bash
conda env update
```

### Aktiver omgivelsene
```bash
conda activate dat801
```

### Installer en Jupyter kernel

```bash
python -m ipykernel install --user --name dat801 --display-name "DAT801"
```

### Test din installasjon
Ved å kjøre følgende kommando åpnes det et nettleservindu. Trykk på `0.0-test.ipynb` for å åpne test-notebooken.
```bash
jupyter notebook
```


## Oppdateringer

Nytt innhold vil legges til i repositoriet underveis i kurset. Kjør følgende kommandoer regelmessig for å sikre at du har siste versjon av innholdet:

* Oppdater kode: 
```bash
cd dat801
git pull
``` 

* Oppdater omgivelser:
```bash
conda activate dat801
conda env update
```


# Troubleshooting
* Hvis du bruker GNU/Linux eller MacOS og kommandoen `conda activate dat801` feiler, kjør `source ~/.bash_profile` og forsøk igjen.
