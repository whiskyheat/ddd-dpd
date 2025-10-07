# Das Dilettantische Duett - Das Perfekte Dinner

## Verlorene Folgen/Wochen
Die ersten Reacts scheinen leider verloren zu sein.
- Stefan aus Gummersbach
- Jürgen


## Zukünftige Ideen
- Statistisch auswerten
- Bewertungen der verlorenen Folgen aus den YT-Videos übernehmen


## Bewertung des Chats
Die Datei `data/bewertungen.csv`enthält unter anderem die durchschnittliche Wertung des Chats.
Diese wurde wie folgt bestimmt:
1. Mittels [twitch-dl](https://github.com/ihabunek/twitch-dl) lassen sich die Chatverläufe der verfügbaren Streams herunterladen.
2. Das Skript `scripts/extract_ratings_from_chat.py` filtert nur die relevanten Messages raus, im Format `time: message`.
3. Das Skript `scripts/cluster_chat_ratings.py` clustert die Messages nach ihrem Zeitstempel, und gibt für jeden Cluster die durchschnittliche Bewertung aus


## Sonstiges
https://github.com/ihabunek/twitch-dl hat eine Funktion zum herunterladen von chats, wenn das video noch verfügbar ist.
