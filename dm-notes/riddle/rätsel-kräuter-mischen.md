# Aufgabe
## Ihr habt die folgenden Kräuter:
- **W**olfswurzel
- **X**enokraut
- **Y**unblüte
- **Z**ittermoss
## Jedes Kraut besitzt einige dieser Eigenschaften:
- **a**phrodisierend
- **b**elebend
- **c**ouragefördernd 
- **d**urchblutungsfördernd
## Mehrere Kräuter zu einem Trank mischen
Eine Eigenschaft ist im Trank vorhanden, wenn sie in ungerader Anzahl unter den verwendeten Kräutern vorkommt. 
## Ziel
Der gesuchte Trank hat alle vier Eigenschaften. 
Welche Kräuter-Kombination ergibt den gesuchten Trank?
# Hinweise
Die Tränke folgender Kombinationen sind euch bekannt:

| Kombination                                     | aphrodisierend | belebend | couragefördernd | durchblutungsfördernd |
| ----------------------------------------------- | :------------: | :------: | :-------------: | :-------------------: |
| **W**olfswurzel + **X**enokraut                 |       ✅        |    ✅     |                 |           ✅           |
| **X**enokraut + **Y**unblüte                    |       ✅        |          |        ✅        |           ✅           |
| **W**olfswurzel + **Y**unblüte + **Z**ittermoss |                |    ✅     |                 |           ✅           |
| **X**enokraut + **Z**ittermoss                  |                |          |        ✅        |                       |
# Klärungen
- Alle Kombinationen der Kräuter sind zudem paralysierend und toxisch, so wie das Spinnentoxin, das neutralisiert werden soll. Der Trank muss mit dem Toxin der Spinne gemischt werden.
- Ein Trank, aus nur einem Kraut ist ungenießbar. Der Trinkende erbricht es und ist vergiftet bis zum Ende der nächsten langen Rast. 
- Mischt man mehr als drei Kräuter erhält man Suppe, keinen Trank.
# Hilfe beim Lösen
Die Helden haben genug Kräuter um 3 Tränke zu brauen. Sie können so Kombinationen erproben. Wenn sie einen Trank trinken, erfahren sie die Eigenschaften des Tranks. Der Trinkende muss eine Konstitutions Rettungswurf (DC 15) machen, bei Fehlschlag ist er vergiftet bis zum Ende der nächsten langen Rast. Zudem würfelt er einen W4 um zu ermitteln, welches Körperteil für eine Stunde paralysiert ist. 
1. rechter Arm
2. rechtes Bein
3. linkes Bein
4. linker Arm
# Lösung
**W**olfswurzel + **Z**ittermoss = 1100 + 0011 = 1111 = Heiltrank

|                           | Wolfswurzel | Xenokraut | Yunblüte | Zittermoss |
| ------------------------- |:-----------:|:---------:|:--------:|:----------:|
| **a**phrodisierend        |      1      |     0     |    1     |     0      |
| **b**elebend              |      1      |     0     |    0     |     0      |
| **c**ouragefördernd       |      0      |     0     |    1     |     1      |
| **d**urchblutungsfördernd |      0      |     1     |    0     |     1      |
## Lösungsweg
Hinweise: 
```
1. W + X = 1101
2. X + Y = 1011
3. W + Y + Z = 0101
4. X + Z = 0010
```
Zu jedem Hinweise kann man vier Gleichungen aufstellen, je eine für jede Eigenschaft.
```
1. W + X = 1101
	1. Wa + Xa = 1 -> Wa ≠ Xa -> Wa = Xa+1
	2. Wb + Xb = 1 -> Wb ≠ Xb -> Wb = Xb+1
	3. Wc + Xc = 0            -> Wc = Xc
	4. Wd + Xd = 1 -> Wc ≠ Xc -> Wd = Xd+1
2. X + Y = 1011
	1. Xa + Ya = 1 -> Xa ≠ Ya -> Ya = Xa+1
	2. Xb + Yb = 0            -> Yb = Xb
	3. Xc + Yc = 1 -> Xc ≠ Yc -> Yc = Xc+1
	4. Xd + Yd = 1 -> Xd ≠ Yd -> Yd = Xd+1
3. W + Y + Z = 0101
4. X + Z = 0010
	1. Xa + Za = 0            -> Za = Xa 
	2. Xb + Zb = 0            -> Zb = Xb
	3. Xc + Zc = 1 -> Xc ≠ Zc -> Zc = Xc+1
	4. Xd + Zd = 0            -> Zd = Xd
```
In die Gleichung vom dritten Hinweis setzt man nun ein.
```
3. W + Y + Z = 0101
	1. Wa + Ya + Za = Xa+1 + Xa+1 + Xa   = 0
	2. Wb + Yb + Zb = Xb+1 + Xb   + Xb   = 1
	3. Wc + Yc + Zc = Xc   + Xc+1 + Xc+1 = 0
	4. Wb + Yb + Zb = Xd+1 + Xd+1 + Xd   = 1
```
Zwei gleiche Werte (z.B. `Xb + Xb`) kürzen sich jeweils raus. Daraus folgt:
```
Xa = 0
Xb+1 = 1 -> Xb = 0
Xc = 0
Xd = 1
X = 0001
```
Jetzt da man X kennt, kann man es einfach in die anderen Gleichung einsetzen und erhält W, Y, Z.