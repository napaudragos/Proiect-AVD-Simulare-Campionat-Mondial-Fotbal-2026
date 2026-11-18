# ⚽ Simulare Campionatul Mondial de Fotbal 2026

Proiect de **Analiza și Vizualizarea Datelor** (în echipă cu Rădulescu Darius): prezicem câștigătoarea Cupei Mondiale 2026 din date reale și analizăm cum sunt văzuți jucătorii în presa sportivă.

## Partea 1: Predicția turneului (`Proiect_AVD_Part1.py`)
- **Web scraping** asincron (Playwright) a peste 1.600 de meciuri internaționale de pe Flashscore, îmbogățite cu valoarea loturilor de pe Transfermarkt.
- **Curățarea datelor:** corectarea inversărilor Home/Away, eliminarea coloanelor cu peste 60% valori lipsă și completarea xG lipsă cu un **Random Forest Regressor**.
- **Power Index** propriu: valoarea lotului și rank-ul FIFA (30%), rezultatele reale (30%), statisticile din teren (40%).
- **Clustering K-Means** pe stiluri de joc și un **Random Forest Classifier** (acuratețe de 58%) care simulează tot turneul, meci cu meci, până la finală.

## Partea 2: Analiza presei sportive (`Proiect_AVD_Part2.py`)
- Extragerea știrilor de pe Flashscore, curățarea textului și împărțirea lui în propoziții.
- **Analiză de sentiment** cu un model Transformer (**XLM-RoBERTa**) pe propozițiile care menționează jucători de top.
- **Dashboard** interactiv: hărți choropleth, WordCloud pe forma țării, bubble charts și grafice de polarizare.

## Tehnologii
Python · Pandas · scikit-learn · Playwright · BeautifulSoup · Hugging Face Transformers · Plotly · GeoPandas · Google Colab

## Documentație
Rezultatele și graficele sunt în prezentarea [`Analiza Campionatului Mondial de Fotbal 2026 Final.pptx`](Analiza%20Campionatului%20Mondial%20de%20Fotbal%202026%20Final.pptx).
