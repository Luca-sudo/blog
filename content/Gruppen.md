---
tags: mathe-1 
draft: true
---

Wenn wir bspw. mit den ganzen Zahlen rechnen, dann haben wir einige Eigenschaften die es leichter machen; gucken wir uns dazu mal an, was man bei der Multiplikation von Bruechen so machen kann.

1. Es ist egal, ob ich $\frac{1}{2}*(\frac{1}{3}*\frac{1}{4})$ oder $(\frac{1}{2}*\frac{1}{3})*\frac{1}{4}$ rechne. Beides liefert das Gleiche Ergebniss.
2. Es gilt $\frac{1}{2}* 1 = \frac{1}{2}$ - mit Eins multiplizieren aendert nichts am Ergebniss.
3. Ich kann fuer jede Zahl einen Kehrwert finden. Habe ich also $\frac{1}{2}$, so kann ich Zaehler und Nenner vertauschen (den Kehrwert bilden), und erhalte $\frac{2}{1}$. Nun gilt insbesonders $\frac{1}{2}*\frac{2}{1}= 1$.

Das sind drei Eigenschaften die das Rechnen mit Bruechen angenehm machen. Die gute Nachricht: Wenn Du diese drei Eigenschaften verstanden hast, dann weisst du bereits was <mark style="background: #FF5582A6;">Gruppen</mark> sind!
Wie es in der Mathematik ueblich ist, sind wir nicht nur an einem Fall interessiert. Wir haben uns zuvor Brueche bezueglich Multiplikation angeschaut, nun wollen wir abstrahieren und definieren die Eigenschaften einer Gruppe bezueglich einer beliebigen Operation $*$. Diese meint damit nicht Multiplikation, sondern soll eine Art Stellvertreter fuer eine konkrete Operation bei einer konkreten Gruppe sein.

Darueberhinaus fuehren wir gruppentypische Notation ein. So schreiben wir fuer ein Element, welches die 2. Eigenschaft oben erfuellt - sprich, ein Element welches das Ergebniss nicht aendert - $e$ und nennen dies das *neutrale Element*. Fuer das was vorher der Kehrwert war haben wir auch einen Namen und eine Notation. Dies nennen wir das *Inverse Element*, und schreiben es als $x^{-1}$. 

1. <mark style="background: #ABF7F7A6;">Assoziativitaet</mark>: $\forall a,b,c \in G : a + (b + c) = (a + b) + c$.
2. <mark style="background: #ABF7F7A6;">Neutrales Element</mark>: $\exists e \in G : \forall g \in G : e + g = g$. 
3. <mark style="background: #ABF7F7A6;">Inverses Element</mark>: $\forall g \in G : \exists (-g) \in G : g + (-g) = e$.

>[!caution] Achtung
>Haeufig denken Studis, wenn Assoziativitaet eingefuehrt wird, dass man die Reihenfolge der Zahlen tauschen kann - das ist nicht der Fall. Wenn wir mit ganzen Zahlen rechnen, dann koennen wir auch die Reihenfolge vertauschen, in Gruppen ist dies allgemein aber nicht der Fall!
>Die Eigenschaft, dass man die Reihenfolge vertauschen kann, nennt man Kommutativitaet. Diese Eigenschaft gilt nicht fuer alle Gruppen, und wir werden diese noch genauer betrachten.
