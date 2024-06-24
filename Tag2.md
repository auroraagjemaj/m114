# Wir beschäftigen uns hier mit sogenannten Baumstrukturen. Kennen Sie noch andere Gebiete in der IT, wo Baumstrukturen zur Anwendung kommen? 

Beim Huffman handelt es sich sogar um eine spezielle Baumstruktur, nämlich einen sogenannten binären Baum. Was unterscheidet einen binären Baum von einem nicht-binären Baum?

# binärer Baum vs. !binärer Baum:

Ein binärer Baum ist dadurch gekennzeichnet, dass jeder Knoten höchstens zwei Kinder hat. Es gibt nur Verzweigungen mit zwei abzweigenden Ästen.

# Wo kommen Baumstrukturen zur Anwendung?
Datenbanken: Baumstrukturen wie B-Bäume und B+-Bäume werden genutzt, um Indizes zu organisieren und eine schnelle Datensuche zu ermöglichen.
Dateisysteme: Hierarchische Dateisysteme verwenden Baumstrukturen, um die Organisation von Ordnern und Dateien zu strukturieren.
Compilerbau: Abstrakte Syntaxbäume (AST) dienen dazu, die Struktur von Quellcode während der Kompilierung darzustellen.

Aufgabe:
# Wie könnte die Komprimierung ausschauen, wenn es sich anstatt um ein Schwarz/Weißbild, um ein Farbbild handelt? Benachbarte Pixel mit identischer Farbe werden ja bei RLC bekanntlich nicht einzeln genannt, sondern zu einer Anzahl zusammengefasst wie z.B. 11xGrün, 6xBlau, 3xWeiß etc. oder in binärer Schreibweise 1011Grün, 0110Blau, 0011Weiß. Welche Bitbreite (1011Grün ergäbe 4 Bit) wäre bei einem quadratischen Bild mit 20 Pixel Kantenlänge sinnvoll? Was wäre, wenn dieses Bild nur aus einer Farbe besteht?

Antwort:
Wenn nur eine Farbe im Bild dargestellt wird, wäre es sinnvoll, pro Zeile 5 Bit zu verwenden. Da jedoch dieselbe Farbe 400 Mal vorkommt, können wir diese Information effizienter in einem Code speichern. Die Bitlänge für die Zahl 400 im binären System beträgt 9 Bit.

Wenn jedoch jeder Pixel eine andere Farbe hat, benötigt man zwar nur ein Bit pro Farbe, aber insgesamt viel mehr Speicherplatz. Das bedeutet, dass man 20 Bit pro Zeile und insgesamt 400 Bit für das ganze Bild benötigt.

4. RLC
Aufgabe:
# Sie erhalten diesen RL-Code: 010100011110010010010010010010010010010110010110010010010010010010010010001. Folgendes ist Ihnen dazu bekannt: Es handelt sich um eine quadratische Schwarz/Weiß-Rastergrafik mit einer Kantenlänge von 8 Pixel. Es wird links oben mit der Farbe Weiß begonnen. Eine Farbe kann sich nicht mehr als siebenmal wiederholen. Zeichnen Sie die Grafik auf. Was stellt sie dar?

Code-Analyse:
010 100 011 110 010 010 010 010 010 010 010 010 010 110 010 110 010 010 010 010 010 010 010 010 001
| | | | | | | | | | | | | | | | | | | | | | | | |
2 4 3 6 2 2 2 2 2 2 2 2 2 6 2 6 2 2 2 2 2 2 2 2 1
| | | | | | | | | | | | | | | | | | | | | | | | |
W S W S W S W S W S W S W S W S W S W S W S W S W
Es wird ein 'A' dargestellt.

5. LZW-Verfahren
Aufgabe:
# a. Erstellen Sie die LZW-Codierung für das Wort „ANANAS“ und überprüfen Sie mit der Dekodierung Ihr Resultat.

LZW-Codierung:
Zeichenkette	Gefunden	Gespeichert	Eintrag	Nummer
ananas	a	a	an	256
nanas	n	n	na	257
anas	a	256	ana	258
as	a	a	as	-
Resultat:
ANANAS = an256as

Aufgabe:
# b. Versuchen Sie den erhaltenen LZW-Code „ERDBE<256>KL<260>“ zu dekomprimieren.

LZW-Dekodierung:
Zeichenkette	Gefunden	Ausgabe	Eintrag	Nummer
erdbe256kl260	e	e	-	-
rdbe256kl260	r	r	er	256
dbe256kl260	d	d	rd	257
be256kl260	b	b	db	258
e256kl260	e	e	be	259
256kl260	e	er	ee	260
kl260	k	k	ek	261
l260	l	l	kl	262
260	e	ee	le	263
Resultat:
ERDBE<256>KL<260> = erdbeerdklee
