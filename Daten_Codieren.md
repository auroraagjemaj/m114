### Aufgaben

## 1. Erstellen Sie eine leere Tabelle mit 6 Kolonnen und 16 Zeilen. Füllen Sie diese wie folgt aus:
 1. Kolonne: Dezimalzahlen von 0 bis 15
 2. Kolonne: Hexadezimalzahlen von 0 bis F
 3. Kolonne, 4. Kolonne, 5. Kolonne und 6. Kolonne: die entsprechenden Binärzahlen

Studieren Sie nun Ihre fertig ausgefüllte Tabelle, insbesondere die Kolonnen mit den 
Binärwerten. Was stellen Sie fest?

#### Lösung

| Dezimal | Hexadezimal | Binär  | Binär  | Binär  | Binär  |
|---------|-------------|--------|--------|--------|--------|
| 0       | 0           | 0000   | 0000   | 0000   | 0000   |
| 1       | 1           | 0001   | 0001   | 0001   | 0001   |
| 2       | 2           | 0010   | 0010   | 0010   | 0010   |
| 3       | 3           | 0011   | 0011   | 0011   | 0011   |
| 4       | 4           | 0100   | 0100   | 0100   | 0100   |
| 5       | 5           | 0101   | 0101   | 0101   | 0101   |
| 6       | 6           | 0110   | 0110   | 0110   | 0110   |
| 7       | 7           | 0111   | 0111   | 0111   | 0111   |
| 8       | 8           | 1000   | 1000   | 1000   | 1000   |
| 9       | 9           | 1001   | 1001   | 1001   | 1001   |
| 10      | A           | 1010   | 1010   | 1010   | 1010   |
| 11      | B           | 1011   | 1011   | 1011   | 1011   |
| 12      | C           | 1100   | 1100   | 1100   | 1100   |
| 13      | D           | 1101   | 1101   | 1101   | 1101   |
| 14      | E           | 1110   | 1110   | 1110   | 1110   |
| 15      | F           | 1111   | 1111   | 1111   | 1111   |

Ich stelle fest, dass ich vier Kolonnen für Binärzahlen benötigte, die jedoch alle denselben Wert enthalten. Dies ergibt wenig Sinn, da jede Zahl nur einmal benötigt wird.

Das Dezimalsystem ist das "normale" Zahlensystem, das wir im Alltag verwenden.

Das Hexadezimalsystem basiert auf der Basis 16 statt 10 wie beim Dezimalsystem.

Das Binärsystem besteht nur aus den Ziffern "0" und "1". Die erste Stelle von rechts hat den Wert 1. Dieser Wert verdoppelt sich nach links hin. Wenn die Ziffer eine "1" ist, wird dieser Wert gezählt; bei einer "0" nicht. Zum Beispiel: 0101 = 0 + 4 + 0 + 1 = 5 (Dezimal und auch Hexadezimal hier).

## 2. Wandeln Sie die folgende Dezimalzahl ohne Taschenrechner in die entsprechende Binärzahl um: 911

### Rechenweg

911 = 512 + 256 + 128 + 8 + 4 + 2 + 1 = 911

512 + 256 = 768
768 + 128 = 896
896 + 8 = 904 
904 + 4 + 2 + 1 = 911 

(Es gibt auch einen anderen Rechenweg, bei dem man die Zahl durch 2 teilt und den Rest, der nur 0 oder 1 sein kann, notiert, um die Binärzahl zu erhalten)

### Lösung

911 = 0011 1000 1111

## 3. Wandeln Sie die folgende Binärzahl ohne Taschenrechner in die entsprechende Dezimalzahl um: 1011'0110

### Rechenweg

1011 0110 = 2 + 4 + 16 + 32 + 128 = 182

### Lösung

1011 0110 = 182

## 4. Wandeln Sie die folgende Binärzahl ohne Taschenrechner in die entsprechende Hexadezimalzahl um: 1110'0010'1010'0101

### Rechenweg

1110 0010 1010 0101

1110 = E
0010 = 2
1010 = A
0101 = 5

### Lösung

1110 0010 1010 0101 = E2A5

## 5. Was ergibt die Addition der beiden binären Zahlen 1101'1001 und 0111'0101?
Beachten Sie, dass für das Resultat ebenfalls nur 8 Binärstellen zur Verfügung stehen.

### Rechenweg

```
  1101 1001
+ 0111 0101
-----------
1 0100 1110
```

Da nur 8 Binärstellen für das Ergebnis zur Verfügung stehen, wird der Übertrag ignoriert. Die Lösung lautet also:

### Lösung

0100 1110

## 6. Was könnten die beiden folgenden binären Werte bedeuten?
(Tipp: a. ins Dezimalsystem umrechnen, b. ins Hexadezimalsystem umrechnen)

### a. 1100’0000.1010’1000.0100’1100.1101’0011

1100'0000 -> 192
1010'1000 -> 168
0100'1100 -> 76
1101'0011 -> 211

Also:
1100'0000.1010'1000.0100'1100.1101'0011 = 192.168.76.211 

192.168.76.211 sieht aus wie eine IP-Adresse.

### b. 1011’1110-1000’0011-1000’0101-1101’0101-1110’0100-1111’1110

1011'1110 -> BE
1000'0011 -> 83
1000'0101 -> 85
1101'0101 -> D5
1110'0100 -> E4
1111'1110 -> FE

Also:
1011'1110-1000'0011-1000'0101-1101'0101-1110'0100-1111'1110 = BE-83-85-D5-E4-FE

BE-83-85-D5-E4-FE sieht aus wie eine MAC-Adresse.

## 8. Dimensionieren Sie für den Matterhorn-Express, wo insgesamt 107 Gondeln die Touristen von Zermatt auf den Trockenen Steg befördern, die Codebreite des Binärcodes für die Kabinenzählung.

### Rechenweg

107 = 0110 1011

### Lösung 

Es werden 7 Stellen für den Binärcode benötigt.

## 9. Sie untersuchen einen Arbeitsspeicher mit 12-Bit-Adress- bzw. 16-Bit-Datenbus. Welche Speicherkapazität in kiB besitzt dieser? (Hinweis: 1kiB=1024B)

### Rechenweg und Lösung

2^12 = 4'096 
4096 * 16 Bit = 65'536 Bits

65'536 / 8 = 8'192 Bytes

8'192 / 1024 = 8 KiB

Der Arbeitsspeicher besitzt eine Speicherkapazität von 8 KiB.

## 10. Zwei Geräte sind mit einer seriellen Leitung und zusätzlichem Taktsignal verbunden. Das Taktsignal beträgt 1MHz.

### a. Wie viele Bytes können damit pro Sekunde übertragen werden?

1 MHz / 8 Bits = 125 kBytes pro Sekunde

### b. Wie viele Bytes pro Sekunde könnten übertragen werden, wenn die Verbindung der beiden Geräte nicht seriell, sondern 8 Bit parallel wäre?

Genau gleich, da 8 Bits gesendet werden, also ein Byte. Da die Taktfrequenz immer noch 1 MHz ist, werden pro Takt 8 Bits (parallel) versendet. Also wieder:

1 MHz = 1 MB/s (8-Bit-parallel).

## 13. Erstellen Sie die Wahrheitstabellen für die folgenden Funktionen:

### a. Logisch UND/AND (mit zwei Eingangs- und einer Ausgangsvariablen)
| Eingang A | Eingang B | Ausgang |
|-----------|-----------|---------|
| 0         | 0         | 0       |
| 0         | 1         | 0       |
| 1         | 0         | 0       |
| 1         | 1         | 1       |

### b. Logisch ODER/OR (mit zwei Eingangs- und einer Ausgangsvariablen)
| Eingang A | Eingang B

 | Ausgang |
|-----------|-----------|---------|
| 0         | 0         | 0       |
| 0         | 1         | 1       |
| 1         | 0         | 1       |
| 1         | 1         | 1       |

### c. Logisch NICHT/NOT (mit einer Eingangs- und einer Ausgangsvariablen)
| Eingang | Ausgang |
|---------|---------|
| 0       | 1       |
| 1       | 0       |

### d. Logisch EXOR (mit zwei Eingangs- und einer Ausgangsvariablen)
| Eingang A | Eingang B | Ausgang |
|-----------|-----------|---------|
| 0         | 0         | 0       |
| 0         | 1         | 1       |
| 1         | 0         | 1       |
| 1         | 1         | 0       |

## 14. Eine in der Computertechnik wichtige mathematische Funktion ist die Restwert- oder Modulo-Funktion mit dem in z.B. Java und C verwendeten Operationszeichen %. 

Versuchen Sie nun, die folgenden Berechnungen auszuführen. Was stellen Sie fest?

- a. 11 % 2 = 1
- b. 10 % 2 = 0
- c. 10 % 3 = 1
- d. 10 % 5 = 0
- e. 10 % 9 = 1

### Antwort:

Die Modulo-Operation (%) berechnet den Rest einer Division der ersten Zahl durch die zweite. Wenn der Rest 0 ist, bedeutet dies, dass die erste Zahl ohne Rest durch die zweite teilbar ist. Ansonsten ergibt sich der Rest der Division als Ergebnis der Modulo-Operation.
