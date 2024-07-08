# Aufgaben

## 1. Huffman-Algorithmus: 

### Binärer Baum vs. Nicht-binärer Baum

Ein binärer Baum hat pro Knoten nur zwei Kinder, das heißt, es gibt nur Astgabeln mit zwei abstammenden Ästen.

### Anwendungen von Baumstrukturen:

- Datenbanken
- Dateisysteme
- Compilerbau

## 2. Huffman-Algorithmus:

### Aufgabe:
1. Jeder denkt sich ein Wort mit ca. 15 Buchstaben aus.
2. Erstellen Sie den Huffman-Code inkl. Codetabelle und das entsprechend komprimierte Wort in Binärdarstellung.
3. Tauschen Sie die Codes und Codetabellen aus und vergewissern Sie sich, dass der Partner das gewählte Wort richtig dekomprimieren kann.
4. Zeigen Sie einen korrekten binären Baum, die Codes tabellarisch und das komprimierte Wort in Huffman-Binärcode.

## 3. RLC (Run Length Coding):

### Frage: Wie könnte die Komprimierung ausschauen, wenn es sich anstatt um ein Schwarz-Weiß-Bild um ein Farbbild handelt?

### Antwort:
Bei einem quadratischen Bild mit 20 Pixel Kantenlänge könnte man folgende Bitbreiten verwenden:
- Wenn nur eine Farbe im Bild dargestellt wird, würde es Sinn ergeben, pro Zeile 5 Bit zu verwenden. Da aber 400 mal die gleiche Farbe vorkommt, können wir dies in einem Code speichern. Die Bitlänge für die Zahl 400 im binären Zahlenraum beträgt: 9 Bit.
- Wenn jeder Pixel eine andere Farbe hat, benötigt man zwar nur einen Bit pro Farbe, dafür aber insgesamt viel mehr. Das bedeutet 20 Bit pro Zeile -> 400 Bit für das ganze Bild.

## 4. RLC:

### Frage: Sie erhalten diesen RL-Code: 010100011110010010010010010010010010010110010110010010010010010010010010001. Es handelt sich um eine quadratische Schwarz-Weiß-Rastergrafik mit einer Kantenlänge von 8 Pixel. Es wird links oben mit der Farbe Weiß begonnen. Zeichnen Sie die Grafik auf. Was stellt sie dar?

### Lösung:
```
010 100 011 110 010 010 010 010 010 010 010 010 010 110 010 110 010 010 010 010 010 010 010 010 001
 |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
 2   4   3   6   2   2   2   2   2   2   2   2   2   6   2   6   2   2   2   2   2   2   2   2   1
 |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |   |
 W   S   W   S   W   S   W   S   W   S   W   S   W   S   W   S   W   S   W   S   W   S   W   S   W

WWSSSSWW
WSSSSSSW
WSSWWSSW
WSSWWSSW
WSSSSSSW
WSSSSSSW
WSSWWSSW
WSSWWSSW
```
Es wird ein 'A' dargestellt.

## 5. LZW-Verfahren:

### a. Erstellen Sie die LZW-Codierung für das Wort „ANANAS“ und überprüfen Sie mit der Dekodierung Ihr Resultat.

| Zeichenkette | Gefunden | Gespeichert | Eintrag | Nummer |
| ------------ | -------- | ----------- | ------- | ------ |
| ananas       | a        | a           | an      | 256    |
| nanas        | n        | n           | na      | 257    |
| anas         | a        | 256         | ana     | 258    |
| as           | a        | a           | as      | -      |

ANANAS = an256as

### b. Versuchen Sie den erhaltenen LZW-Code „ERDBE<256>KL<260>“ zu dekomprimieren.

| Zeichenkette  | Gefunden | Ausgabe | Eintrag | Nummer |
| ------------- | -------- | ------- | ------- | ------ |
| erdbe256kl260 | e        | e       | -       | -      |
| rdbe256kl260  | r        | r       | er      | 256    |
| dbe256kl260   | d        | d       | rd      | 257    |
| be256kl260    | b        | b       | db      | 258    |
| e256kl260     | e        | e       | be      | 259    |
| 256kl260      | e        | er      | ee      | 260    |
| kl260         | k        | k       | ek      | 261    |
| l260          | l        | l       | kl      | 262    |
| 260           | e        | ee      | le      | 263    |

ERDBE256KL260 = ERDBEERDKLEE

## 6. BWT (Burrows-Wheeler-Transformation):

### a. Erstellen Sie die BWT-Transformation für das Wort ANANAS und überprüfen Sie mit der Rücktransformation Ihr Resultat.

### b. Sie erhalten den Code IICRTGH6 in der Burrows-Wheeler-Transformation. Welches Wort verbirgt sich dahinter?

## 6. ZIP-Komprimierung: 

### a. Erstellen Sie ASCII-Textdateien mit folgenden Längen: 10, 100, 1000, 10'000, 100'000 Zeichen.

### b. Achten Sie darauf, dass die Zeichen möglichst zufällig gewählt werden. Nutzen Sie Textgeneratoren aus dem Internet.

### c. Kopieren Sie jede dieser fünf Textdateien in eine eigene ZIP-Datei und werten Sie die Speichergrößen aus.

### d. Erstellen Sie eine Excel-Tabelle mit den Größenverhältnissen: ASCII-Dateigröße zu ZIP-Dateigröße und interpretieren Sie die Ergebnisse grafisch.

### e. Erstellen Sie eine ASCII-Textdatei mit 100'000 Zeichen, ausschließlich mit dem Buchstaben A. Zippen Sie diese Datei und vergleichen Sie die Speichergrößen mit der zufällig befüllten Datei. Erklären Sie den Unterschied.

### f. Untersuchen Sie die ZIP-Komprimierung bei bereits komprimierten Dateien (JPG-Bilder). Nutzen Sie die folgenden Bilder:
https://www.juergarnold.ch/Kompression/ZIPTestHi.jpg
https://www.juergarnold.ch/Kompression/ZIPTestLo.jpg

Gehen Sie vor wie bei den Textdateien und begründen Sie das Resultat.

## 7. Weitere verlustlose Komprimierungsverfahren:

### Frage: Welche Daten sollten verlustlos komprimiert werden? Was würde passieren, wenn man einen Brief oder Java-Sourcecode verlustbehaftet komprimieren würde?

### Antwort:
Verlustlose Komprimierung ist wichtig für Daten, bei denen jede Information entscheidend ist, wie bei Textdokumenten, Quellcode, Datenbanken und medizinischen Bildern. Verlustbehaftete Komprimierung würde bei solchen Daten zu Informationsverlust führen und den Inhalt unbrauchbar machen.
