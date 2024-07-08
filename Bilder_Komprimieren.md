# Aufgaben

## 1. Um ein gewisses Verständnis für die Luminanz-Chrominanz-Beschreibung von Farben zu erhalten, lösen Sie die folgenden Aufgaben. 

Benutzen Sie dazu dieses Online-Tool: [Colorizer](https://colorizer.org/)

### Codes übersetzen: 

- RGB 255/255/255 entspricht Weiß und ergibt in YCbCr: Y=1, Cb=0, Cr=0
- RGB 0/0/0 entspricht Schwarz und ergibt in YCbCr: Y=0, Cb=0, Cr=0
- Y=0, Cb=0.5, Cr=0 entspricht der Farbe: Rot
- Y=0, Cb=-0.5, Cr=0 entspricht der Farbe: Grün
- Y=0, Cb=0, Cr=0.5 entspricht der Farbe: Blau
- Y=0, Cb=0, Cr=-0.5 entspricht der Farbe: Dunkelgrün
- Y=0.3, Cb=0.5, Cr=-0.17 entspricht der Farbe: Hellrot

## 2. Ein RGB-Farbbild benutzt nur die Farbe Weiß als Hintergrund und ein Hellblau mit folgenden Werten: R=33, G=121, B=239 (8 Bit pro Farbkanal). Das Bild soll in ein Graustufenbild umgewandelt werden. Berechnen Sie den für das Hellblau entsprechenden Grauwert. (8 Bit pro Farbkanal)

### Lösung:

Für das Hellblau mit den RGB-Werten R=33, G=121, B=239 wäre der Grauwert:

Grauwert = (R * 0.3) + (G * 0.6) + (B * 0.1)

Grauwert = (33 * 0.3) + (121 * 0.6) + (239 * 0.1)

Grauwert = 9.9 + 72.6 + 23.9

Grauwert = 106.4

## 3. Berechnen Sie, wieviel Speicher eingespart wird, wenn ein Bild mit Subsampling 4:1:1 komprimiert wird.

### Lösung:

Bei Subsampling 4:1:1 wird die Farbaufzeichnung auf ein Viertel reduziert, während die Luminanz vollständig erhalten bleibt. Das bedeutet, dass der Speicherbedarf für die Farbinformationen auf 1/4 reduziert wird.

Die Einsparung beträgt somit 3/4 des Speichers für die Farbinformationen.
