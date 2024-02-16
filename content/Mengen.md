---
tags:
  - mathe-1
draft: true
---
Mengen sind der fundamentale Begriff in der Mathematik. Alles, was Ihr macht, benutzt Mengen als Grundlage. Deshalb ist ein gutes Verstaendnis davon, was eine Menge ist, bzw. was keine Menge ist, so wichtig. 

# Motivation
Egal was wir rechnen oder beweisen werden, es wird immer um eine zugrundeliegende Menge gehen. Mal sind das bspw. die ganzen Zahlen ($\mathbb{Z}$) - was gut ist, da wir die laengste Zeit mit Zahlen gerechnet haben - mal sind dies aber schwerer greifbare Objekte.[^1] Insbesonders sind Funktionen, wie wir sie aus der Schule kennen, Vorschriften wie man Objekte aus einer Menge auf Objekte aus einer anderen Menge abbildet. 

Was ist also eine Menge? Wann sind zwei Mengen gleich? Gibt es unendlich grosse Mengen? Wie kann man Mengen kombinieren? All das sind Fragen, die wir im Folgenden klaeren werden. Bevor wir das tun, muessen wir erstmal Mengen definieren.

# Definition


> [!quote] Menge
> Eine Menge ist ein Objekt, welches aus der Zusammenfassung einer Anzahl einzelner Objekte hervorgeht.[^2]

Was soll mir dieser Satz sagen? Zum einen ist eine Menge eine Zusammenfassung von mehreren Objekten; Objekte sind hier bewusst nicht weiter spezifiziert, da alles vorstellbare ein Objekt sein kann. Beispielsweise kann ich meinen Kuehlschrankinhalt zu einer Menge zusammenfassen, dieser besteht beispielsweise aus: Eiern, Milch, Kaese und Salat. Um schonmal an die mathematische Notation zu gewoehnen schreibe ich dies wie folgt: $\{\text{Eier, Milch, Kaese, Salat}\}$. Dies definiert mir dann eine Menge.

Eine wichtige Besonderheit liegt darin, dass wir doppelte, identische Elemente ignorieren. Das bedeutet konkret, dass es fuer die Charakterisierung der Menge egal ist, wieviele Eier ich  im Kuehlschrank habe; das einzig wichtige ist, dass ich welche habe. Anders formuliert sind also $\{\text{Eier, Milch, Kaese, Salat}\}$ und $\{\text{Eier, Eier, Milch, Kaese, Salat}\}$ *die selbe Menge*! Eine Menge wird also nicht durch ihre Zusammensetzung aus Elementen definiert, sondern genauer gesagt durch die Zusammensetzung aus einzigartigen Elementen.

# Komische Eigenschaften

Nun kommt ein weiterer Teil der Definition, welcher erstmal komisch wirkt. Nach der Definition ist "eine Menge ein Objekt", was also bedeutet, dass wir eine Menge aus Mengen bauen koennen. Nehmen wir einfach mal an, es gaebe nur zwei Fakultaeten an einer Universitaet, die Informatik Fakultaet und die Philosophie Fakultaet. Ausserdem hat unsere fiktive Universitaet ganze 5 Studierende! Diese sind wie folgt aufgeteilt, Marie und Jan sind beide an der Fakultaet fuer Informatik, und Max, Jenny und Karl sind an der Philosophie Fakultaet. Nun kann ich die Studierenden beider Fakultaeten, jeweils als Mengen angeben. So erhalten wir $\{\text{Marie, Jan}\}$ fuer die Informatik Fakultaet, und $\{\text{Max, Jenny, Karl}\}$ fuer die Philosophie Fakultaet. 

Nun kann ich beide Menge wieder kombinieren, und erhalte $\{\{\text{Marie, Jan}\}, \{Max, Jenny, Karl\}\}$, was wieder eine Menge ist. Das allein ist u.U. komisch, wenn man es das erste mal sieht, keine Sorge. Eine interessante Frage, die man nun stellen kann ist die Folgende: Sind die Mengen $\{\{\text{Marie, Jan}\}, \{\text{Max, Jenny, Karl}\}\}$ und $\{\text{Marie, Jan, Max, Jenny, Karl}\}$ identisch? Die Antwort lautet nein, was, jenachdem wie man die Mengen betrachtet hat, unsinnig erscheint. Ich sehe zwei Arten diese Mengen zu betrachten, entweder indem man sich die Studierenden anguckt, welche in beiden Mengen vorhanden sind, oder indem man sich die *Elemente* der Menge anguckt.

Wenn wir uns die Studierenden angucken, welche in beiden Mengen vorhanden sind, dann macht sich das Gefuehl breit, dass die Mengen identsich sind. Wenn wir uns aber die *Elemente* der beiden Mengen angucken, so koennen wir erkennen, dass die Mengen nicht gleich sein koennen. Die erste Menge hat zwei Elemente, die Menge der Informatik Studierenden, und die Menge der Philosophie Studierenden. Die zweite Menge hat 5 Elemente, das sind die einzelnen Studierenden. Wir haben also zwei Mengen, die eine unterschiedliche Anzahl an eindeutigen Elementen haben - die Mengen koennen also nicht identisch sein.

Der Unterschied, den wir gerade betrachtet haben, ist essenziell fuer das Verstaendnis von [[Potenzemengen]], da man bei der Potenzmenge von einer Menge bestehend aus Mengen spricht, dies ist aehnlich zu unserem Beispiel hier.

# Operationen auf Mengen

Im vorherigen Abschnitt habe ich an einem Punkt die Menge der Informatikstudierenden und der Philosophiestudierenden *vereint*. Sprich, ich habe die beiden Mengen so kombiniert, dass ich in der resultierenden Menge alle Elemente aus *beiden* Mengen habe. Das ist ein Beispiel fuer eine Operation auf Mengen, die man *Vereinigung* nennt. Wir wollen nun einige der Operationen einfuehren.

## Vereinigung

Wenn ich zwei Mengen $A, B$ habe, dann ist die *Vereinigung* von $A$ und $B$ die Menge, welche die Elemente von $A$ und $B$ enthaelt. 


> [!info] Vereinigung
> Wir definieren die Vereinigung von Mengen wie folgt:
> $$A \cup B := \{x | x \in A \vee x \in B\}$$

## Durchschnitt

Beim Durchschnitt betrachte ich alle Elemente die *sowohl* in der einen, *als auch* in der anderen Menge liegen. Der wichtige Unterschied zu der Vereinigung liegt darin, dass wir bei der Vereinigung ausschliesslich fordern, dass die Elemente in mindestens einer der Mengen liegen; beim Durchschnitt fordern wir, dass die Elemente in beiden Mengen liegen.


> [!info] Vereinigung
> Wir definieren den Durchschnitt von Mengen wie folgt:
> $$A \cap B := \{x | x \in A \wedge x \in B\}$$


## Teilmenge

Manchmal will man beschreiben, dass eine Menge $A$ in einer anderen Menge $B$ liegt. Das bedeutet genauer, dass alle Elemente aus $B$ auch Elemente aus $A$ sind. Nehmen wir mal ein Beispiel: Die Menge $B$ sind alle Studierenden an einer Universitaet, und die Menge $A$ sind alle Studierenden der Sozialwissenschaften. Es ist klar, dass alle Studierenden, die Sozialwissenschaften studieren, insbesonders auch Studierende an der Uni sind, weshalb sie ebenfalls in der Menge $B$ sind.


> [!info] Teilmenge
> Eine Menge $B$ ist eine Teilmenge von $A$, geschrieben $B \subset A$, genau dann wenn
> $$\forall x \in B : x \in A$$

Die Definition spiegelt genau das, was wir vorher beschrieben haben. *Jedes* Element in $B$ ist auch ein Element in $A$; jeder SoWi Studierende ist auch ein Student.

## Komplement

Wenn wir eine Menge haben, dann koennen wir an allen Elementen interessiert sein, die *nicht* in dieser Menge liegen. Um das Beispiel der SoWi Studierenden zu nutzen bestuende das Komplement dieser Menge aus allen Studierenden die *nicht* SoWi studieren. Ein wichtiges Detail fehlt hier noch. Immer wenn wir ein Komplement einer Menge bilden, dann tun wir dies *relativ* zu einer uebergeordneten Menge. Hier war implizit klar, dass wir von einer Gesamtmenge aller Studierenden sprechen, im allgemeinen ist aber nicht immer klar von welcher Grundmenge man spricht. Wenn ich Euch die Menge $\{1, 2, 3\}$ gebe, und Euch bitte das Komplement zu berechnen, dann koennt ihr das nicht unmittelbar. Manche wuerden hier alle natuerlichen, manche alle ganzen Zahlen, und manche alle Reellen Zahlen als Grundmenge betrachten. Deshalb: *Immer darauf achten, was die Grundmenge ist.*


> [!info] Komplement
> Sei $A \subset B$, dann bezeichnen wir mit $A^c$ das Komplement von $A$, welches wie folgt definiert ist:
> $$A^c = \{x \in B : x \notin A\}$$

# Potenzmenge


# Verstaendnisfragen
1. Angenommen $A \subset B$, gilt dann $B^{c}\subset A^{c}$? Warum?
2. Was muss fuer $B$ gelten, damit $A \subset (A \cap B)$ gilt?
# Uebungsaufgaben
1. Beweise die folgenden Aussagen:
	- $(A \cap B) \subset A$
	- $A \subset (A \cup B)$
	- $(A \cap B) \subset (A \cup B)$
2. Beweise, dass $(A^c)^c=A$.
3. Beweise, dass $(A \cap B)^{c} = A^{c} \cup B^{c}$.
4. Gilt auch $(A \cup B)^{c}= A^{c} \cap B^{c}$? Warum?



[^1]: Wenn wir von Zahlen sprechen, dann haben die Meisten eine *Intuition*, da man sein ganzes Leben schon mit Zahlen gerechnet hat. Ab dem Moment, wo man ueber komischere Objekte spricht, wird es umso wichtiger, zu wissen, was eine Menge ist.
[^2]: Von Wikipedia geklaut: https://de.wikipedia.org/wiki/Menge_(Mathematik)
[^3]: Falls nicht klar ist warum das gilt, so empfehle ich Euch selbst davon zu ueberzeugen.