Word Model
==========
Warum Simulation
----------------
- Gebäudebau: Nicht möglich eine Prototyp zu bauen
- Bar kann nicht nachträglich vergrössert / verkleinert werden
- Zu kompliziert zum Rechen, weil zu viele Variablen + keine Lust
- Testen unmöglich -> Statisten würden beim Warten sterben, würden dick vom vielen Futtern oder würden verhungern bim Warten uf die Bestellung oder würden an der Bar zu viele Drinks nehmen und wären zu betrunken zum Tisch zu wechseln.


Ansturm
-------
Zu findende Verteilungen: 
- über der Zeit: Zwei Peaks -> Scedule
- gleichzeit auftretende Anzahl Leute: Leute kommen in Pärchen, zu dritt, viert, ... -> Poisson Verteilung
- Queue draussen vor der Tür sollte möglichst leer sein


Konzept
-------
Als Ausgangskonzept wird das Hardrock in Atlanta City verwendet.

Bar:
Die Bar dient als Warteschlange bis ein Tisch frei wird.
Servierpersonal an der Bar wird nicht berücksichtigt. Grund dafür ist eine fixe Anzahl Barpersonal.

Ziel ist es, dass an der Bar möglichst viele Plätze besetzt sind, weil diese Konsumenten konsumieren und Umsatz bescheren. Gleichzeitig sollte vor der Türe die Schlange möglichst klein oder gar nicht existieren, damit niemand an der Kälte warten muss, bzw wieder geht. Die Wartezeit an der Bar sollte nicht mehr als ein bis zwei Drinks betragen, damit niemand wieder geht, bevor ein Tisch frei wird.
Drinklänge: ca. eine Viertelstunde.

Tische:
Am Tischen werden ein bis drei Gänge gegessen -> Verteilfunktion.
Als erstes soll eine Simulation einfach gehalten werden:
Servierdüse kommt einmal und bedient -> belegte Ressource für best. Zeit -> Verteilfunktion.
Teller und Karte bringen soll erst in einem zweiten Schritt modelliert werden, je nach Zeit.
- In der Realen Welt bestehen die Tische aus zweiertischen und die ankommenden Gruppen müssen auf Vielfache von Zweierplätzen aufgeteilt werden. Dabei kann es zu leeren Plätzen kommen. Der Einfachheit halber soll dies nicht berücksichtigt werden in der Simulation.
- Die Plätze werden fix gewählt anhand des Beispiels von Atlantic City. -> 250 Plätze

Küche:
Erster Schritt: Keine Küche, nur bestimmte Wartezeit bis Essen fertig+gebracht.
Verschiedene Köche, die pro Essen / Gang eine Bestimmte Zeit gebunden sind -> Verteilfunktion.
Essen ist eine Ressource.

Anschliessend kehren die Gäste nach Hause zurück und der Tisch wird frei für neue Gäste.
Optional könnten einige Gäste erneut an die Bar zurückkehren.


Objectives
==========
Vor der Türe:
Queue: Ankommende Gäste lim(0)

Küche
-----
Resources: 
Agents: Köche

Bedienung:
---------
Agents: Servierdüsen, Tellerbringer

Bar:
---
Queue: Anzahl Warteplätze

Tisch:
-----
Resourcen: Anzahl Plätze


If Questions
============
Ziel ist die Gewinnmaximierung durch gute Auslastung. Als gute Auslastung wird 75% Utilisation angenommen.
Wie gross muss die Bar sein, damit fast niemand an der Kälte warten muss und die mittlere Aufenthaltszeit an der Bar ein bis zwei Drinks nicht übersteigt.
Wie viel Servierersonal, Köche und wie viele (Tellerbringer) braucht es, damit die Mittlere Aufenthaltszeit am Tisch bei ca. 1.5 Stunden liegt.


Spezifikationen
===============
Gearbeitet wird mit Fiktiven Daten, Ausnahme #Plätze im Saal.

Restaurant mit 
- Queuelänge
- #Servierpersonal
- #Köche
- Gruppen mit untersch. # Leuten

Ermittelt werden soll:
- Aufenthaltszeit in Queue
- Dauer des Aufenthaltes
- Utilisation der Agents


Zusatzprojekt (optional):
- # Barpersonal
- Kochzeit genauer / unterschiedliche Kochzeiten für unterschiedliche Gänge
- #Tellerbringer
- Gruppen müssen an den gleichen Tisch