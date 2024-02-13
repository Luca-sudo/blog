---
tags: mathe-1 
draft: true
---

Gruppen sind eines der Themen, welches am schwersten zu greifen ist, wenn im ersten Semester soviel abstrakte Mathe auf einen geworfen wird. Dieser gesamte Beitrag soll mehreres bezwecken:
1. Wir wollen zuerst einen gemeinsamen Nenner finden; dafuer schauen wir uns an wie wir mit Bruechen rechnen. Dies ist ein Sprungbrett in das Thema Gruppen.
2. Die Definition von Gruppen verstehen, und Eigenschaften von Gruppen betrachten.
3. An Gruppen wiederholen wie man einen Beweis skizziert und strukturiert. Bzw., wie man versteht was man genau beweisen soll.

# Rechnen mit Bruechen

Wenn wir bspw. mit den ganzen Zahlen rechnen, dann haben wir einige Eigenschaften die es leichter machen; gucken wir uns dazu mal an, was man bei der Multiplikation von Bruechen so machen kann.

1. Es ist egal, ob ich $\frac{1}{2}*(\frac{1}{3}*\frac{1}{4})$ oder $(\frac{1}{2}*\frac{1}{3})*\frac{1}{4}$ rechne. Beides liefert das Gleiche Ergebniss.
2. Es gilt $\frac{1}{2}* 1 = \frac{1}{2}$ - mit Eins multiplizieren aendert nichts am Ergebniss.
3. Ich kann fuer jede Zahl einen Kehrwert finden. Habe ich also $\frac{1}{2}$, so kann ich Zaehler und Nenner vertauschen (den Kehrwert bilden), und erhalte $\frac{2}{1}$. Nun gilt insbesonders $\frac{1}{2}*\frac{2}{1}= 1$.

Das sind drei Eigenschaften die das Rechnen mit Bruechen angenehm machen. Die gute Nachricht: Wenn Du diese drei Eigenschaften verstanden hast, dann weisst du bereits was <mark style="background: #FF5582A6;">Gruppen</mark> sind!

# Was ist eine Gruppe?

Wie es in der Mathematik ueblich ist, sind wir nicht nur an einem Fall interessiert. Wir haben uns zuvor Brueche bezueglich Multiplikation angeschaut, nun wollen wir abstrahieren und definieren die Eigenschaften einer Gruppe bezueglich einer beliebigen Operation $*$. Diese meint damit nicht Multiplikation, sondern soll eine Art Stellvertreter fuer eine konkrete Operation bei einer konkreten Gruppe sein.
Wichtig hier ist, dass die Verknuepfung zwei Elemente aus $G$ nimmt, und diese wieder auf ein Element in $G$ abbildet. Wir bleiben also mit der Verknuepfung in der urspruenglichen Gruppe $G$. Dies ist eine gute Moeglichkeit das Lesen von Funktionssignaturen zu ueben. Um zu zeigen, dass die Verknuepfung zwei Elemente in $G$ nimmt, und ein Element in $G$ zurueckgibt, schreiben wir folgende Signatur.

$$
* : G \times G \to G
$$

Darueberhinaus fuehren wir gruppentypische Notation ein. So schreiben wir fuer ein Element, welches die 2. Eigenschaft oben erfuellt - sprich, ein Element welches das Ergebniss nicht aendert - $e$ und nennen dies das *neutrale Element*. Fuer das was vorher der Kehrwert war haben wir auch einen Namen und eine Notation. Dies nennen wir das *Inverse Element*, und schreiben es als $x^{-1}$. 

1. <mark style="background: #ABF7F7A6;">Assoziativitaet</mark>: $\forall a,b,c \in G : a * (b * c) = (a * b) * c$.
2. <mark style="background: #ABF7F7A6;">Neutrales Element</mark>: $\exists e \in G : \forall g \in G : e * g = g$. 
3. <mark style="background: #ABF7F7A6;">Inverses Element</mark>: $\forall g \in G : \exists g^{-1} \in G : g * g^{-1} = e$.

>[!caution] Achtung
>Haeufig denken Studis, wenn Assoziativitaet eingefuehrt wird, dass man die Reihenfolge der Zahlen tauschen kann - das ist nicht der Fall. Wenn wir mit ganzen Zahlen rechnen, dann koennen wir auch die Reihenfolge vertauschen, in Gruppen ist dies allgemein aber nicht der Fall!
>Die Eigenschaft, dass man die Reihenfolge vertauschen kann, nennt man Kommutativitaet. Diese Eigenschaft gilt nicht fuer alle Gruppen, und wir werden diese noch genauer betrachten.

Wichtig ist, zu verstehen, dass eine Gruppe nicht nur aus einer Menge besteht, sondern auch eine Verknuepfung besitzt. In der Definition war diese Verknuepfung $*$, in dem Beispiel zu Beginn des Beitrags war die Verknuepfung die gewoehnliche Multiplikation von Zahlen. 
Wenn wir die Verknuepfung aendern, so kann es sein, dass die Menge mit der neuen Verknuepfung *keine* Gruppe ist. Dazu ein paar Fragen, welche Du als Uebung selbst beantworten sollst.

> [!example] Fragen
> Welche der Folgenden Mengen, mit der gegebenen Verknuepfung, formen Gruppen?
> - $(\mathbb{Z}, +)$
> - $(\mathbb{Z}, \cdot)$
> - $(\mathbb{R}, \cdot)$

Falls Du mit der Beantwortung Probleme hast, keine Sorge. Hier ein kleiner Hinweis: Damit etwas eine Gruppe ist muessen alle drei Eigenschaften von Gruppen gelten. Umgekehrt ist etwas *keine* Gruppe, wenn eine der Eigenschaften *nicht* gilt. Das kann bspw. bedeuten, dass es kein Inverses Element gibt, es kein neutrales Element gibt, oder aber Assoziativitaet nicht gilt. 


# Untergruppen

Wir haben nun gesehen was eine Gruppe ist. Aehnlich wie bei Mengen, wo wir uns fuer Teilmengen interessiert haben, koennen wir uns nun an Gruppen interessieren die selbst in einer groesseren Gruppe liegen. Nehmen wir als Beispiel die ganzen Zahlen $\mathbb{Z}$ mit der Addition, diese formen eine Gruppe. Gibt es eine Teilmenge von $\mathbb{Z}$, welche selbst wieder eine Gruppe ist? Die Antwort ist ja, und wir werden uns ein Beispiel angucken, um Untergruppen ein wenig besser zu verstehen.

Betrachten wir einmal die *geraden* ganzen Zahlen, welche wir mit $2\mathbb{Z}$ notieren. Die Frage, ob diese Menge nun eine Untergruppe von $(\mathbb{Z}, +)$ ist, laesst sich in zwei Fragen aufteilen. 
1. Wenn ich zwei gerade Zahlen addiere, ist das Ergebniss wieder eine gerade Zahl?
2. Erfuellt die Menge der geraden Zahlen alle Gruppeneigenschaften bezueglich der Addition?

Die Eigenschaft, welche in der ersten Frage postuliert wird, nennt man auch *Abgeschlossenheit*. Wir wollen also pruefen, ob die Addition, mit der Signatur $+ : \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$, sich auch auf die geraden Zahlen einschranken laesst, sodass wir $+ : 2\mathbb{Z} \times 2\mathbb{Z} \to 2\mathbb{Z}$ erhalten.
Das koennen wir wie folgt pruefen: 
1. Wir nehmen $a, b \in 2 \mathbb{Z}$
2. Wir rechnen $a + b$, was wir umschreiben koennen zu $2a' + 2b'$.[^1] 
3. Nun nutzen wir die Distributivitaet in $\mathbb{Z}$, und erhalten $2a'+2b' = 2(a' + b')$, womit wir fertig sind. Wir haben eine Zahl, welche sich schreiben laesst als $2$ mal irgendeine andere Zahl.


[^1]: Da wir wissen, dass sowohl $a$ als auch $b$ gerade sind, koennen wir diese schreiben als $2$ mal eine andere Zahl. Das tun wir hier, fuer $a = 2a'$ und $b = 2b'$.