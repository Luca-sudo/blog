---
tags:
  - mathe-1
draft: true
---

Gruppen sind eines der Themen, welches am schwersten zu greifen ist, wenn im ersten Semester soviel abstrakte Mathe auf einen geworfen wird. Dieser gesamte Beitrag soll mehreres bezwecken:
1. Wir wollen zuerst einen gemeinsamen Nenner finden; dafuer schauen wir uns an wie wir mit Bruechen rechnen. Dies ist ein Sprungbrett in das Thema Gruppen.
2. Die Definition von Gruppen verstehen, und Eigenschaften von Gruppen betrachten.
3. An Gruppen wiederholen wie man einen Beweis skizziert und strukturiert. Bzw., wie man versteht was man genau beweisen soll.

Gruppen tauchen in unerwarteten Kontexten auf. Beispielsweise begegnen einem diese bei der Betrachtung von [[Permutation|Permutationen]], wodurch man die [[Symmetriegruppe]] erhaelt.

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

## Untergruppenkriterium

Um zu pruefen, ob $2\mathbb{Z}$ die Eigenschaften einer Gruppe erfuellt koennen wir einen Satz ausnutzen, und uns Rechnerei sparen.


> [!important] Untergruppenkriterium
> Sei $(G, *)$ eine Gruppe, und $U \subset G$. Dann ist $(U, *)$ eine Untergruppe genau dann, wenn fuer alle $a, b \in U : a*b^{-1} \in U$ und $U \neq \emptyset$.

Wenn wir sagen, dass dieses Kriterium fuer Untergruppen genuegt, dann meinen wir damit, dass aus diesem Kriterium alle drei Eigenschaften von Gruppen folgen. Warum dies so ist, wollen wir uns genauer angucken. Zuerst fangen wir mit der Assoziativitaet an.

Wir haben gegeben, dass $(G, *)$ eine Gruppe ist. Also gilt fuer alle Elemente in $G$ Assoziativitaet - insbesondere gilt Assoziativitaet auch fuer alle Elemente in $U \subset G$. Somit gilt fuer alle Elemente in $U$ Assoziativitaet, die erste Eigenschaft konnten wir also folgern.

Als Naechstes wollen wir sehen, dass auch die Existenz von Inversen folgt. Wir wollen also zeigen, dass wenn $a \in U$, dann folgt, dass auch $a^{-1}$ in $U$. Dafuer nutzen wir das Untegruppenkriterium, aber mit $e$ und $a$.[^2] Setzen wir dies in die Gleichung ein, so erhalten wir $e * a^{-1}$, was gleich $a^{-1}$ ist. Somit erhalten wir also fuer ein beliebiges Element $a \in U$ auch das Inverse $a^{-1} \in U$.

Zu guter letzt wollen wir uns die Existenz vom neutralen Element anschauen. Dies folgt jedoch einem aehnlichen Argument wie das Inverse. Wir nutzen das Untegruppenkriterium mit $a$ und erhalten $a * a^{-1} = e \in U$.

Bleibt noch die Frage warum die Teilmenge *nichtleer* sein muss. Das hat eine rein logische Begruendung. Wenn die Teilmenge leer ist, dann kann ich eine mehr oder weniger beliebige Aussage machen, und diese stimmt. Das liegt daran, dass es kein Element in der Menge gibt. Das gibt jedoch bei der Existenz des neutralen Elements ein Problem: Hier muessen wir mindestens ein Element $a \in U$ haben, damit wir daraus das neutrale Element "konstruieren"[^3] koennen.


> [!caution] Achtung
> Wir haben soeben nur gezeigt, dass wenn das Untergruppenkriterium gilt, dann ist $U$ eine Untergruppe. Da der Satz jedoch sagt, dass $U$ eine Untergruppe ist, genau dann wenn $U$ das Untergruppenkriterium erfuellt, muessten wir ansich noch die Rueckrichtung beweisen. Dies eignet sich gut als Uebung.

Nun wenden wir das Untergruppenkriterium an, um zu beweisen, dass $2\mathbb{Z}$ eine Untergruppe von $(\mathbb{Z}, +)$ ist. Der erste Schritt ist leicht: die Menge $2\mathbb{Z}$ ist nichtleer, da $2 \in 2\mathbb{Z}$. Was zu zeigen bleibt ist, dass $\forall a,b \in 2\mathbb{Z} : a+b^{-1} \in 2\mathbb{Z}$. Bevor wir das tun ist wichtig, sich zwei Dinge nochmal vor Augen zu fuehren. Erstens ist $b^{-1} = -b$, durch die Definition von Addition. Zweitens ist $a - b \in 2\mathbb{Z}$, wenn man $a-b$ schreiben kann als $2(a' - b')$, wobei $a', b' \in \mathbb{Z}$.

Wir fangen mit $a-b$ an. Dies koennen wir umschreiben, da $a, b \in 2\mathbb{Z}$. So erhalten wir $2a' - 2b'$. Nun schmeissen wir Distributivitaet drauf, und erhalten $2(a' - b')$, womit wir bereits am Ziel sind. Die geraden Zahlen sind also eine Untergruppe!


> [!example] Uebungsaufgabe
> Beweise, oder wiederlege, dass die *ungeraden* Zahlen eine Untergruppe von $(\mathbb{Z}, +)$ sind. 
>
> *Tipp: ungerade Zahlen kann man schreiben als* $2k + 1$ *fuer ein geeignetes k*.




[^1]: Da wir wissen, dass sowohl $a$ als auch $b$ gerade sind, koennen wir diese schreiben als $2$ mal eine andere Zahl. Das tun wir hier, fuer $a = 2a'$ und $b = 2b'$.
[^2]: In der Definition des Untegruppenkriteriums nutzen wir also statt einem allgemeinen $a$ das neutrale Element $e$, und anstatt $b$ das Element $a$.
[^3]: Konstruieren ist vielleicht ein ungluecklich gewaehltes Wort. Was ich damit meine ist, dass wir das neutrale Element erhalten, indem wir ein Element $a \in U$ auf das Untergruppenkriterium schmeissen. Wenn wir dieses Element $a$ nicht haben, dann haben wir auch keine Moeglichkeit das neutrale Element mit dem Untegruppenkriterium herzuleiten.