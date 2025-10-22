Dein Wunsch ist mir Befehl <:KEKW:949369164810842163> 

## Messwerte
Laut  [dieser Playlist](<https://www.youtube.com/playlist?list=PLerzsTW-w1DiNtTpNwV4XqaV69_Pi9P-l>) gibt es 5 Wochen mit Übernachtung; vier mit jeweils fünf Teilnehmern, und unsere Woche von gestern. 
Wir nummerieren die Kandidaten von 1 bis 5 durch, in der Reihenfolge in der sie kochen.
Die Tabelle enthält für die 4 Wochen welcher Kandidat bei wem übernachten darf/muss. (In Klammern sind die entsprechenden Videos der Playlist.)
```
|                 | 1   | 2   | 3   | 4   | 5   |
| --------------- | --- | --- | --- | --- | --- |
| W1 (17-13)      | 3   | 3   | 1   | 1   | 2   |
| W2 (12-8)       | 4   | 5   | 5   | 2   | 3   |
| W3 (6-2)        | 5   | 1   | 5   | 1   | 4   |
| W4 (1)          | 3   | 5   | 2   | 2   | 2   |
|                 |     |     |     |     |     |
| Murphys Law (7) | 2   | 3   | 4   | 1   |     |
```
Um zu berücksichtigen, dass man nicht bei sich selber übernachten kann, benennen wir um in ABCD: A ist dabei die erste Person, die übernachten kann, D die letzte.  Am 2. Tag können 1345 übernachten, deshalb ist an diesem Tag A=1, B=3, C=4, D=5.
```
|                 | 1   | 2   | 3   | 4   | 5   |
| --------------- | --- | --- | --- | --- | --- |
| W1 (17-13)      | B   | B   | A   | A   | B   |
| W2 (12-8)       | C   | D   | D   | B   | C   |
| W3 (6-2)        | D   | A   | D   | A   | D   |
| W4 (1)          | B   | D   | B   | B   | B   |
|                 |     |     |     |     |     |
| Murphys Law (7) | A   | B   | C   | A   |     |
```

## Analyse
Wir ignorieren die 4er Woche im Folgenden.

Wir wollen überprüfen, ob die Zahnbürste "fair rubbelt", also ob es für jeden gleich wahrscheinlich ist zu übernachten. Anschaulich sollte jeder Buchstabe gleichhäufig auftauchen. Dies ist unsere Nullhypothese.
Insgesamt gibt es 20 Übernachtungen. Jeder Buchstabe sollte (unter der Nullhypothese) mit Wahrscheinlichkeit 1/4 auftauchen, also 5 mal.
```
|                | A   | B   | C   | D   |
| -------------- | --- | --- | --- | --- |
| Beobachtet (B) | 4   | 8   | 2   | 6   |
| Erwartet (E)   | 5   | 5   | 5   | 5   |
| (B-E)^2        | 1   | 9   | 9   | 1   |
```
Die Werte sind recht nah an unserer Erwartung. Um es statistisch genau zu machen, können wir einen [Chi-Quadrat-Test](<https://de.wikipedia.org/wiki/Chi-Quadrat-Test#Verteilungstest>) durchführen. Dafür summiert man hier die Werte für (B-E)^2 und teilt diese durch 5, also X^2 = 20 / 5 = 4, Unter der Nullhypothese, wenn alles fair ist, sollte X^2 eine Chi-Quadrat-Verteilung mit 3 (= 4-1) Freiheitsgraden haben. Bei einem Signifikanzniveau von 95% können wir aus [einer Tabelle](<https://www.crashkurs-statistik.de/tabelle-chi-quadrat-verteilung/>) den Wert 7,815 ablesen. Weil X^2 = 4 < 7,815 ist, kann die Nullhypothese nicht abgelehnt werden. **Es gibt keinen statistisch signifikanten Hinweis auf Manipulation.**

Hinweis:  Man kann sich drüber streiten, ob der Chi-Quadrat-Test hier angebracht ist. Die erwartete Häufigkeit ist mit 5 im Grenzbereich der Anwendbarkeit des Tests.

Die Zahnbürste rubbelt für alle gleich. "Murphys Law" war (höchstwahrscheinlich) Zufall.
