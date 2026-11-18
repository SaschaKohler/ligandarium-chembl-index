# Ligandarium ChEMBL Target Index

Ein kleiner, abgeleiteter Auszug aus der [ChEMBL-Datenbank](https://www.ebi.ac.uk/chembl/) (Version 37): für 15 Zielproteine die bekannten Liganden mit Affinitätswerten. Die Datei wird von der Lern-App *Ligandarium* (Pharmazie und Biochemie, macOS) mitgeliefert und hier offen veröffentlicht.

*A small derived extract of ChEMBL 37: known ligands and affinities for 15 target proteins, used by the macOS teaching app Ligandarium and published here openly.*

## Inhalt

`chembl_targets.json` enthält je Zielprotein:

| Feld | Bedeutung | Herkunft |
|---|---|---|
| `chembl`, `name`, `organism` | ChEMBL-Target-ID, bevorzugter Name, Organismus | ChEMBL |
| `label` | deutscher Anzeigename | eigene Ergänzung |
| `pdb` | PDB-Beispielstrukturen, die in der App verwendet werden | eigene Ergänzung |
| `ligands[].chembl`, `name`, `phase`, `smiles` | Molekül-ID, Name, höchste klinische Phase, SMILES | ChEMBL |
| `ligands[].type`, `pchembl`, `nM`, `n` | Messart (Ki/Kd/IC50/EC50), Median-pChEMBL, Median in nM, Anzahl der Messungen | ChEMBL, **berechnet** |
| `measured` | Anzahl der Messwerte, aus denen die Ligandenwerte des Ziels stammen | ChEMBL, berechnet |

Das Feld `source` der Datei nennt Quelle und Lizenz.

## Was wurde gegenüber ChEMBL verändert?

- Auswahl von 15 Zielproteinen (insgesamt 490 Liganden); alle übrigen ChEMBL-Daten fehlen.
- Je Molekül und Ziel wurde der **Median** des pChEMBL-Werts über alle Messungen gebildet (nur Ki, Kd, IC50, EC50 mit Relation „=“). Das ist keine Originalmessung.
- Je Ziel sind zugelassene Wirkstoffe sowie die potentesten weiteren Liganden aufgenommen.
- Deutsche Anzeigenamen und PDB-Verweise wurden ergänzt.

Die Werte sind Näherungen für die Lehre, nicht klinisch validiert und keine Wirkungsaussage.

## Lizenz und Namensnennung

Diese Datei ist eine Bearbeitung von ChEMBL-Daten und steht wie ChEMBL unter **[Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/)**, siehe [LICENSE](LICENSE). Du darfst sie auch kommerziell nutzen, wenn du

1. ChEMBL nennst, z. B.: *Data from ChEMBL 37, EMBL-EBI, licensed under CC BY-SA 3.0; modified (subset, medians)*,
2. die Lizenz verlinkst und Änderungen kenntlich machst,
3. Bearbeitungen unter derselben Lizenz weitergibst.

Bitte zitiere ChEMBL: Zdrazil B. et al., *The ChEMBL Database in 2023: a drug discovery platform spanning multiple bioactivity data types and time periods*, Nucleic Acids Research 2024, 52(D1), D1180–D1192.

Diese Lizenz gilt nur für die Datendatei. Die App *Ligandarium* selbst (Quellcode, Oberfläche, übrige Daten) ist **nicht** Teil dieses Repositories und steht nicht unter CC BY-SA.

Dieses Projekt ist nicht mit EMBL-EBI verbunden und wird von ihr nicht unterstützt.

## Kontakt

Sascha Kohler, Apotheker in Österreich.
