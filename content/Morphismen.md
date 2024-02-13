---
draft: true
tags:
  - mathe-1
---
Zuvor hat man sich [[Funktion|Funktionen]] angeguckt, diese hatten mehrere Komponenten, welche wir kurz rekapitulieren. Eine [[Funktion]] $f$ bildet von einer [[Menge]] $A$ auf eine andere [[Menge]] $B$ ab, was wir mit $f : A \to B$ beschreiben. Solche [[Funktion|Abbildungen]] koennen beliebig aussehen. Was wenn ich mir nun [[Funktion|Abbildungen]] anschaue, welche eine bestimmte strukturelle Eigenschaft haben. Dafuer schauen wir uns ein motivierendes, wenn auch kuenstliches, Beispiel an.

Wir betrachten die Abbildung $f : \mathbb{R} \to \mathbb{R}$ mit $f(x) = 2^x$. Erstmal ist das eine ganz normale [[Funktion|Abbildung]]. Wenn wir uns aber an die [[Potenzgesetze]] erinnern, dann sehen wir, dass wir folgendes tun koennen: $2^{3 + 4} = 2^{3} * 2^{4}$. Wenn wir das bezueglich der Funktion $f$ aufschreiben, so erhalten wir $f(3 + 4) = f(3) * f(4)$ - wir koennen die Funktion "auseinanderziehen".[^1] 
Wir sehen also, dass wir vor Anwenden der Abbildung Addieren koennen, oder nach Anwendung der Abbildung multiplizieren koennen. Da wir mittlerweile Experten in Sachen [[Gruppen]] sind praezisieren wir die Signatur der [[Funktion|Abbildung]], und erhalten $f: (\mathbb{R}, +) \to (\mathbb{R}, \cdot)$. 

Wir haben soeben unseren erstem *Morphismus* betrachtet. Wie wir sehen werden definiert die Abbildung $f$ einen *Homomorphismus*. 

# Definition

S

 [^1]:  Ich bin mir sicher, dass diese ausdrucksweise einigen Mathematikern Kopfschmerzen bereiten wird.