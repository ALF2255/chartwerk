# Chartwerk

Kerzencharts für Bitcoin, Ethereum, Solana, Gold und Silber mit Zeichenwerkzeugen,
Echtzeitkursen und Abgleich zwischen Geräten. Installierbar als App (PWA).

## Marktwetten (Kalshi)

Knopf „Marktwetten“ (alle Instrumente: Bitcoin, Ethereum, Solana, Zcash, Gold, Silber, Brent-Öl, EUR/USD – und künftige Kryptowährungen automatisch, soweit Kalshi Kursmärkte dafür hat): zeigt, was Händler auf der US-Prognosebörse Kalshi für den
Kurs zu festen Terminen einpreisen – nächste Stunde, heute/morgen, Woche, Monat, länger. Im Chart erscheint am
Termin eine senkrechte Spanne (80 %-Bereich, Punkt = Mitte), im Kasten zusätzlich die Chance „höher als jetzt“.
Kasten antippen klappt ihn ein und aus. Nur Anzeige. Blockiert der Browser den Abruf, im Kasten eine
Umweg-Adresse eintragen (z. B. ein kleiner Weiterleiter auf dem NAS).

## Hoch/Tief-Wetten (Kalshi)

Eigener Knopf „Hoch/Tief-Wetten“: Kalshi-Wetten darauf, ob der Kurs **bis** zum Termin **irgendwann** eine Marke
erreicht (Höchst- bzw. Tiefststand bis Tag/Woche/Monat/Jahr). Kasten rechts oben mit den Marken für 90 %, 50 % und
10 % Wahrscheinlichkeit; im Chart gepunktete Linie auf der 50:50-Marke bis zum Termin (grün = Hoch, rot = Tief).

## Gaps (Kurslücken)

Knopf „Gaps“: Binance handelt rund um die Uhr, die Börse nicht (Fr 17 Uhr bis So 18 Uhr New Yorker Zeit geschlossen,
also etwa Fr 23 bis So 24 Uhr deutscher Zeit). Mit eingeschaltetem Knopf werden die Wochenend-Kerzen weggelassen – dann
entsteht zwischen Freitagsschluss und Wochenstart die Lücke wie bei TradingView (bei Bitcoin & Co. die bekannte „CME-Lücke“).
Woche und Monat werden dafür aus Tageskerzen gebaut. Offene Lücken erscheinen als Zone (blau = Lücke nach oben,
orange = nach unten), teilweise gefüllte Lücken schrumpfen, geschlossene bleiben als umrandete Fläche „Gap ✓“ sichtbar (vom Entstehen bis zum Schließen). Der Kasten zeigt die
nächsten offenen Lücken mit Abstand zum Kurs und wie oft Lücken innerhalb von 1 Woche, 4 Wochen und 3 Monaten geschlossen
wurden (geschlossen = Kurs wieder auf dem Schluss vor der Lücke). Mindestgröße einstellbar. Feiertage werden nicht
berücksichtigt. Für die Statistik am besten den Zeitrahmen „Tag“ nehmen.

Schalter „Wende nach dem Schließen“ im Gaps-Kasten: wie oft der Kurs 1 W / 4 W / 3 M nach dem Schließen wieder auf der Seite
liegt, von der er in die Lücke kam (also an der Lücke gedreht hat) – im Vergleich zum Zufall (wie oft der Kurs nach derselben
Zeit überhaupt höher bzw. tiefer liegt). Im Chart ein Punkt am Schließ-Niveau: grün = nach 4 Wochen gewendet, rot = weitergelaufen.

## Vollbild

Im Vollbild ist die Knopfleiste ausgeblendet. Oben im Chart neben Instrument und Zeitrahmen gibt es dann „Indikatoren ▾“: eine Liste aller Indikatoren zum An- und Ausschalten (Häkchen = an). Die Liste bleibt offen, bis man daneben tippt.

## Einrichten auf GitHub Pages

1. Auf github.com ein neues Repository anlegen, Name `chartwerk`, Sichtbarkeit **Public**.
2. Im Repository „Add file → Upload files“ und alle Dateien aus diesem Ordner hochladen
   (nicht den Ordner selbst, sondern seinen Inhalt). „Commit changes“.
3. „Settings → Pages“: unter „Branch“ `main` und `/ (root)` wählen, „Save“.
4. Nach ein bis zwei Minuten läuft die App unter `https://DEIN-NAME.github.io/chartwerk/`.

## Installieren

- Android: Adresse in Chrome öffnen, Menü (⋮) → „App installieren“ bzw. „Zum Startbildschirm hinzufügen“.
- PC: Adresse in Chrome oder Edge öffnen, in der Adressleiste auf das Installieren-Symbol klicken.

## Abgleich zwischen Handy und PC

1. github.com → Profilbild → Settings → Developer settings → Personal access tokens → Tokens (classic)
   → „Generate new token (classic)“.
2. Name z. B. `Chartwerk`, Ablauf nach Wunsch, **nur** das Häkchen bei `gist` setzen, erstellen und den Schlüssel kopieren.
3. In Chartwerk: Backup-Symbol (Pfeil nach unten) → Schlüssel einfügen → „Verbinden“.
4. Auf dem zweiten Gerät denselben Schlüssel eintragen. Ab dann gleicht die App automatisch ab.

Der Schlüssel bleibt nur auf deinen Geräten. Die Zeichnungen liegen in einem geheimen Gist in deinem GitHub-Konto.

## Silber

Für Echtzeitkurse bei Silber einen kostenlosen Schlüssel von twelvedata.com im Datenquellen-Fenster
(Knopf „Live“/„Simuliert“ über dem Chart) eintragen.

## Updates

Neue Version von `index.html` im Repository hochladen und ersetzen. Die App holt sie sich beim nächsten Start.
