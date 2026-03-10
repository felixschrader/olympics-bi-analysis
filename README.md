# Olympics BI Analysis

Interaktives Business-Intelligence-Dashboard zur Analyse historischer Olympiadaten (1896–2016).

**→ [Dashboard aufrufen](https://olympics-bi-analysis-5tyzxr4upfrdsun4evxhtc.streamlit.app/)**

---

## Inhalt

Das Dashboard untersucht drei Kernfragen anhand von 166.000+ Athleteneinträgen:

**Körperliches Profil & Medaillenerfolg**  
Zusammenhänge zwischen Größe, Gewicht und BMI und dem Medaillengewinn – aufgeteilt nach Sportart und Geschlecht. Zielgruppe: Trainer.

**Geografie & Gleichstellung**  
Frauenanteil im Zeitverlauf, Verteilung nach Land und Kontinentvergleich. Zielgruppe: Sportverbände.

**Heimvorteil**  
Performance der Gastgeberländer vor, während und nach den Spielen. Zielgruppe: Analysten.

---

## Seiten

| Seite | Beschreibung |
|---|---|
| Übersicht | KPIs, Top-Nationen, Teilnehmertrend |
| Athletenprofil | Interaktive Körperprofile der Medaillengewinner nach Sportart |
| Körper & Medaillen | Alter, Größe, BMI im Vergleich – Gewinner vs. Nicht-Gewinner |
| Geografie & Gleichstellung | Frauenanteil-Trend, Weltkarte, Kontinentvergleich |
| Heimvorteil | Performance-Score vor, während und nach Ausrichtung |

---

## Entwicklung

Konzeption, Datenanalyse und Fragestellungen stammen aus dem Projektverlauf.
Bei der Umsetzung des Streamlit-Dashboards wurde Claude (Anthropic) als
Coding-Assistent eingesetzt.

---

## Stack

- Python 3.12
- Streamlit
- Plotly
- Pandas

---

## Lokale Ausführung

```bash
git clone https://github.com/rexkraemer/olympics-bi-analysis
cd olympics-bi-analysis
pip install -r requirements.txt
streamlit run app.py
```

Die Datei `olympics.csv` muss im Stammverzeichnis liegen (Trennzeichen: Semikolon).

---

## Datenstruktur

| Spalte | Beschreibung |
|---|---|
| ID | Athleten-ID |
| Name | Name |
| Sex | M / F |
| Age | Alter |
| Height | Körpergröße (mm → wird zu m umgerechnet) |
| Weight | Gewicht (100g → wird zu kg umgerechnet) |
| Year | Olympiajahr |
| Sport | Sportart |
| Event | Disziplin |
| Medal | Gold / Silver / Bronze / NaN |
| NOC | Nationaler olympischer Code |
| Country | Land |
