# Auslegung eines Wasserdurchflusskanals

Reynolds-skalierte Auslegung eines geschlossenen Strömungskanals für die Untersuchung eines Tragflächenprofils, von der Profilberechnung bis zur Pumpenspezifikation.

**Kontext:** Tätigkeit als wissenschaftliche Hilfskraft am Institut InEV, Jade Hochschule (Studiengang Maschinenbau M.Eng.)
**Status:** Auslegung und CFD-Validierung abgeschlossen. Der Kanal wurde aus Budgetgründen nicht gebaut.
**Software:** MATLAB, Excel, 3D Experience, Ansys SpaceClaim, Ansys Fluent

## Aufgabe

Ein Wasserkanal sollte in ein bestehendes Wasserbecken passen. Die Beckenabmessungen waren eine feste Randbedingung. Ziel war eine Reynoldszahl von 2.000.000 (bezogen auf die Profilsehne) in der Teststrecke. Testobjekt: NACA 0012 bei 8° Anstellwinkel, bewusst als ungünstigster Fall gewählt.

## Warum Wasser?

Die kinematische Viskosität von Wasser ist rund 15-mal niedriger als die von Luft. Für dieselbe Reynoldszahl an einem kompakten Modell (Sehne ≈ 106,5 mm) wären in Luft über 280 m/s nötig, in Wasser rund 18,9 m/s. Der Luftwert ist ein allgemeiner physikalischer Vergleich zur Einordnung der Entwurfsentscheidung und kein Simulationsergebnis.

## Methodik

1. NACA-0012-Profil bei 8° in MATLAB dargestellt, Extrempunkte ausgewertet.
2. Blockage Ratio 0,06 bezogen auf die Teststrecke (0,3 m × 0,3 m) ergibt die Profilsehne (106,5 mm).
3. Parametrische Excel-Rechnung für Strömungsgeschwindigkeit und Volumenstrom, darauf aufbauend Dimensionierung aller Kanalabschnitte.
4. Geometrie als geschlossener Kreislauf in 3D Experience, Aufbereitung in SpaceClaim.
5. Druckverlustsimulation in Ansys Fluent, daraus die Pumpenspezifikation.

| Größe | Wert |
|---|---|
| Reynoldszahl (Sehne) | 2.000.000 |
| Blockage Ratio | 0,06 |
| Kontraktion, Vergrößerungsfaktor | 6 |
| Diffusor, Faktor / Öffnungswinkel | 4 / 3,5° |
| Abmessungen (L × B × H) | 9.030 × 3.100 × 850 mm |

Kontraktion, Teststrecke, Diffusor, Beruhigungskammer, Honeycomb-Gleichrichter und Umlenkbögen mit Leitschaufeln wurden als ein System dimensioniert.

## Ergebnisse

| Größe | Wert |
|---|---|
| Gesamtdruck Einlass | 54.962,94 Pa |
| Gesamtdruck Auslass | 27.151,23 Pa |
| Druckdifferenz | 27.811,71 Pa |
| Hydraulischer Verlust | 2,84 m |

Pumpenspezifikation: Volumenstrom 1,7 m³/s (≈ 26.930 gpm), Förderhöhe ≈ 3 m (10 ft).

## Erkenntnisse

- Die Wahl des Mediums ist bei kompakten Modellen und hohen Ziel-Reynoldszahlen ein wirksamer Hebel gegen unrealistische Anströmgeschwindigkeiten.
- Blockage Ratio, Modellgröße und Pumpenanforderung sind eng gekoppelt.
- Eine feste Bauraumvorgabe verändert die Auslegungsreihenfolge gegenüber einem freien Neubau.

## Repository-Inhalt

Dieses Repository dokumentiert die Auslegung. Berechnungsdateien und Fluent-Daten sind nicht enthalten, sofern nicht ausdrücklich ergänzt.

Portfolio mit Abbildungen: <https://pouria-kamali.de/projekt-wasserkanal.php>
