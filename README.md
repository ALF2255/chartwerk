# Chartwerk

Kerzencharts für Bitcoin, Ethereum, Solana, Gold und Silber mit Zeichenwerkzeugen,
Echtzeitkursen und Abgleich zwischen Geräten. Installierbar als App (PWA).

## Marktwetten (Kalshi)

Knopf „Marktwetten“ (nur Bitcoin, Ethereum, Gold): zeigt, was Händler auf der US-Prognosebörse Kalshi für den
Kurs zu festen Terminen einpreisen – nächste Stunde, heute/morgen, Woche, Monat, länger. Im Chart erscheint am
Termin eine senkrechte Spanne (80 %-Bereich, Punkt = Mitte), im Kasten zusätzlich die Chance „höher als jetzt“.
Kasten antippen klappt ihn ein und aus. Nur Anzeige. Blockiert der Browser den Abruf, im Kasten eine
Umweg-Adresse eintragen (z. B. ein kleiner Weiterleiter auf dem NAS).

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
