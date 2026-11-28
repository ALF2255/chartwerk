# Chartwerk

Kerzencharts für Bitcoin, Ethereum, Solana, Gold und Silber mit Zeichenwerkzeugen,
Echtzeitkursen und Abgleich zwischen Geräten. Installierbar als App (PWA).

## Marktwetten (Kalshi)

Knopf „Marktwetten“ (alle Instrumente: Bitcoin, Ethereum, Solana, Zcash, Gold, Silber, Brent-Öl, EUR/USD – und künftige Kryptowährungen automatisch, soweit Kalshi Kursmärkte dafür hat): zeigt, was Händler auf der US-Prognosebörse Kalshi für den
Kurs zu festen Terminen einpreisen – nächste Stunde, heute/morgen, Woche, Monat, länger. Im Chart erscheint am
Termin eine senkrechte Spanne (80 %-Bereich, Punkt = Mitte), im Kasten zusätzlich die Chance „höher als jetzt“.
Kasten antippen klappt ihn ein und aus. Nur Anzeige. Blockiert der Browser den Abruf, im Kasten eine
Umweg-Adresse eintragen (z. B. ein kleiner Weiterleiter auf dem NAS).

## Quelle Kalshi / Polymarket

In den Kästen „Marktwetten“ und „Hoch/Tief-Wetten“ lässt sich unten die Quelle wählen: Kalshi, Polymarket oder beide. Bei „beide“ stehen die Werte untereinander; im Chart sind Kalshi-Spannen rosa, Polymarket-Spannen blau (leicht versetzt), Polymarket-Hoch/Tief-Linien gestrichelt. Polymarket-Daten kommen aus der öffentlichen Gamma-API, abgerufen über denselben Cloudflare-Weiterleiter.

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

## Divergenzen

Knopf **„Divergenzen“** (abschaltbar) und **„Div: RSI / MACD“**: Kurs macht ein höheres Hoch, der Indikator ein tieferes (▼ bärisch, rot) bzw. Kurs tieferes Tief, Indikator höheres (▲ bullisch, grün).
Wendepunkte mit 5 Kerzen links/rechts, Abstand 5–60 Kerzen, erst 5 Kerzen nach dem zweiten Punkt bestätigt (kein Blick in die Zukunft). RSI: bärisch nur ab 50 aufwärts, bullisch nur bis 50; MACD: über bzw. unter null.
Linien im Kurschart und im RSI- bzw. MACD-Fenster. Check in der Kopfzeile: wie oft der Kurs 10 Kerzen nach der Bestätigung in Richtung der Divergenz lag – verglichen mit der Grundrate aller Kerzen („sonst“) – und Ø Veränderung.

## 200-Tage-Linie

Schalter „MA 200 T“: Durchschnitt der letzten 200 Tage (bei Gold, Silber, Öl und Devisen 200 Handelstage), passend zum Zeitrahmen
umgerechnet – im Wochenchart z. B. 29 Wochen bei Krypto, 40 Wochen bei Gold. Die Legende zeigt den Wert und wie weit der Kurs
darüber oder darunter liegt. Auf 1 Std und 4 Std reichen die Daten oft nicht für die volle Länge.

## Vergleich alle Märkte

Knopf **„Vergleich alle Märkte“** (sichtbar, wenn MACD-Signale oder Divergenzen an sind): rechnet die aktuelle Einstellung (Zeiteinheit, MACD-TF, Signale, Ausstieg, Divergenzen) für jeden Markt durch und zeigt eine Tabelle –
bei „Gegensignal“ Anzahl, Ø je Signal, „Zusammen“ (alle Trades hintereinander), „Halten“ (einfach kaufen ab dem ersten Signal), bestes/schlechtestes; bei „Ziel/Stop“ Ziel/Stop und Trefferquote; Divergenzen mit Trefferquote gegen die Grundrate.
Kurse: Twelve Data (falls Schlüssel) bzw. Binance, bis 1000 Kerzen, 15 Minuten zwischengespeichert. Ohne Gebühren, nur Rückblick.

## Edge-Prüfung (wie beim Bot)

Alle Checks zeigen zusätzlich ein Urteil nach denselben Regeln wie beim Bot: jeder abgeschlossene Trade **nach 0,1 % Gebühr je
Ein- und Ausstieg**, mindestens **30 Trades** und **t ≥ 2,5** (t = Ø je Trade geteilt durch Streuung/√Anzahl – wie deutlich der
Durchschnitt über null liegt). Anzeige: **Edge ✓** (belegt), **kein Beleg** bzw. ✗, **zu wenige Trades**.
- EMA-Kasten: Ø je Trade und Edge-Prüfung.
- MACD-Signale: bei „Ziel/Stop“ zählen auch Trades, die vor Ziel oder Stop durch ein neues Signal beendet wurden (Ausstieg zum
  Schlusskurs) – die Trefferquote „Ziel / Stop“ allein wäre geschönt. Gewinnschwelle bei Ziel 3 / Stop 2 ATR: 40 %.
- Divergenzen: als Trade gelesen (Einstieg bei Bestätigung, Ausstieg 10 Kerzen später), dazu Ø-Veränderung im Vergleich zur Grundrate.
- Vergleich alle Märkte: Spalte „Edge“, Spalte „1. | 2. Hälfte“ (t-Wert getrennt für die ältere und die neuere Hälfte der
  Kerzen – eine echte Edge sollte in beiden bestehen) und Zeile „Alle zusammen“ (Trades aller Märkte gemeinsam geprüft).
  Der Vergleich lädt je Markt bis zu 5000 Kerzen.

## Strategie-Suche

Im Fenster „Vergleich alle Märkte“ spielt **„Alle Strategien durchspielen“** 48 Varianten durch: Chart 1 Std / 4 Std / Tag /
Woche × MACD auf Chart- oder nächsthöherem Zeitrahmen × Signale alle / mit Trend / Nulllinie × Ausstieg Ziel/Stop / Gegensignal,
jeweils mit den Trades aller Märkte zusammen, nach Gebühren, sortiert nach t. „robust ✓“ nur, wenn Gesamt und beide Hälften die
Edge-Prüfung bestehen. Eine Zeile antippen stellt die Variante im Chart ein. Dauert etwa 1–2 Minuten (Twelve Data höchstens
alle 10 Sekunden abgefragt, Gratis-Limit 8/Min.).

## Spot-Strategie (nur Kaufen und Verkaufen)

Knopf **„Spot“** (für eigene Käufe, keine Shorts) zeigt KAUF- und VERKAUF-Schilder im Chart, **„Spot: …“** wählt die Regel:
- **Überverkauft:** Kauf, wenn RSI 14 von unter 30 wieder darüber dreht; Verkauf, wenn er von über 70 wieder darunter dreht.
- **Trendfolge:** Kauf, wenn die MACD-Linie über null kreuzt; Verkauf, wenn sie unter null kreuzt.
- **Rücksetzer:** nur über EMA 200 (EMA 50 über EMA 200): Kauf, wenn RSI von unter 40 wieder darüber dreht; Verkauf bei RSI von über 70
  nach unten oder Schluss unter EMA 200.
- **Zyklus** (nur Bitcoin): Kauf ab dem Tief-Fenster des Halving-Zyklus, wenn RSI von unter 40 wieder darüber dreht; Verkauf nur im
  Hoch-Fenster (bei RSI von über 70 nach unten, spätestens am Fensterende), dazwischen halten. Nur zwei vollständige Zyklen in den
  Daten – Orientierung, kein Beleg.
- **Bewertung:** Mayer-Multiple (Kurs ÷ Durchschnitt 200 Tage) im Vergleich zu seinen eigenen Werten der letzten bis zu 4 Jahre:
  Kauf, wenn es zu den tiefsten 10 % gehört und wieder steigt; Verkauf bei den höchsten 5 %, wenn es wieder fällt. Passt sich an
  schwächer werdende Zyklen an, für alle Märkte (am besten Tag oder Woche).
- **★ Fib (eigene Strategie):** die eigene Fib-Methode des Nutzers als Regel. Fib vom Hoch zum ersten großen Tief danach, gültig bis
  zum nächsten Fib (gestrichelt im Chart: Fib 0, Fib 1, 0,5, 0,65 von unten, 1,236). **Fallen:** Verkauf beim Abverkauf unter die 0,5
  (nachdem der Kurs darüber war), wenn die erste Erholung unter der 0,5 scheitert oder die 1,236 bricht. **Steigen:** Kauf, wenn der
  Kurs nach einem Rutsch unter das erste Tief wieder darüber schließt (KAUF · Boden) oder 4 Wochen über der 0,65 schließt
  (KAUF · bestätigt). Hoch und Tief sucht ein Zickzack ohne Blick in die Zukunft, Schwelle 3,5 × Wochen-Schwankung (12–45 %).
  Schalter „Fib-Boden: nur über 200 T“: der Boden-Kauf zählt erst, wenn der Kurs zusätzlich über der 200-Tage-Linie schließt.
  Schalter „Fibs: Zickzack / meine“: statt des Zickzacks rechnet die Regel mit den selbst gezogenen Fibonacci-Zeichnungen dieses
  Marktes (Hoch vor Tief); jeder gilt ab der Kerze nach seinem Tief. Im Rückblick geschönt (nachträglich gezogen), für den aktuellen
  Plan aber genau richtig. Der Zickzack verlangt nach dem ersten Tief eine Erholung von mindestens 15 % (Gold 2026: 3.944 statt 4.404).
  Schalter „Fib-Stopp: 3 Wochen / 1 Woche“ (Standard 3 Wochen): verkauft wird erst nach drei Wochenschlüssen in Folge unter der 1,236 –
  ein knapper einzelner Schluss darunter ist oft nur ein Test der Marke (Gold Nov. 2026: 3.533 unter 3.554, Woche darauf 3.654).

**„Staffel“** (Schalter, gilt für alle Spot-Regeln): beim Kaufsignal nur 1/3 kaufen, je 1/3 per Limit bei −15 % und −30 % unter dem
ersten Kaufkurs nachkaufen (Schild NACHKAUF), verkauft wird alles. Dritte Stufe „Rest bei +10 %“: nicht gekaufte Teile werden
gekauft, sobald der Kurs 10 % über dem ersten Kauf schließt (Schild REST) – damit bleibt bei sofortigem Anstieg kein Geld liegen. Legende zeigt gekaufte Teile und Ø-Einstandspreis.

**„Spot-Check“** vergleicht alle Regeln für den aktuellen Markt und Zeitrahmen mit „einfach halten“ (Rendite, Zeit im Markt, größter
Rückgang, Edge-Prüfung nach Gebühren). Zeile antippen stellt die Regel ein.

## Handy

Die Legende oben im Chart ist auf dem Handy kompakt (Kurs, EMA, MACD-Signal mit Edge-Urteil, letzte Divergenz);
„Details ▸“ klappt alle Angaben auf (Einstellung je Gerät). Indikatoren und ihre Einstellungen (Signale, Ausstieg, TF, Zahnräder,
Vergleich) stecken auf dem Handy im Menü **„Indikatoren ▾“** in der Legende, der Zeitrahmen unter **„Tag ▾“** – so bleibt
mehr Platz für den Chart.

## PC

Der Kurs steht oben neben den Märkten, alle Indikator-Knöpfe sind sichtbar (sie brechen in eine zweite Zeile um, statt seitlich
zu scrollen). Auf niedrigen Bildschirmen (z. B. 1366 × 768) ist die Werkzeugleiste etwas kleiner, damit alles ohne Scrollen passt.
Tastenkürzel: **1–5** Zeitrahmen (1 Std bis Monat), **← →** verschieben (mit Umschalt größere Schritte), **+ −** bzw. **↑ ↓** zoomen,
**R** Ansicht zurücksetzen, **F** Vollbild, **D** Legende mit/ohne Details, **Entf** Auswahl löschen, **Strg+Z** rückgängig.

## Zeichenleiste

Die Werkzeuge stecken in Gruppen (Zeiger, Linien, Fibonacci, Formen, „⋯“ Weitere): antippen wählt das zuletzt benutzte
Werkzeug der Gruppe, nochmal antippen oder lange drücken klappt die Gruppe aus. Am PC und Tablet nur noch eine schmale
Spalte, am Handy eine kurze Leiste unten. Beim Fib-Fächer lassen sich die Werte der Ebenen frei eintragen (z. B. 0,786).

## Einstellungen für alle Märkte

Im Layout-Fenster („Standard“ oben rechts): Häkchen **„Indikatoren & Zeiteinheit für alle Märkte gleich“** – beim Marktwechsel werden die aktuellen Indikatoren (RSI, MACD, Signale, Zickzack, MA …) und die Zeiteinheit mitgenommen; Zeichnungen bleiben je Markt. Knopf **„Jetzt auf alle Märkte übertragen“** für eine einmalige Übernahme. Einstellung gilt je Gerät.

## RSI, MACD und MACD-Signale (Fenster unter dem Chart)

Drei Knöpfe, jeder einzeln abschaltbar (auch im Objektbaum, in „Indikatoren ▾“ und in Layouts gespeichert):
- **RSI** – Ultimate RSI (Länge 14, Glättung TMA, Signal EMA 14) mit Zonen 80 / 50 / 20, über 50 grün, unter 50 rot gefüllt.
- **MACD** – 12/26/9, Linie grün über / rot unter der Signallinie, Histogramm 4-farbig (steigend/fallend über/unter null).
  Knopf „TF“: wie Chart oder **nächsthöherer Zeitrahmen** (z. B. Woche auf dem Tageschart); der laufende Abschnitt wird mit dem aktuellen Kurs gerechnet.
- **MACD-Signale** – BUY/SELL im Chart bei MACD-Kreuzung (aus demselben MACD wie im Fenster, also auch im höheren Zeitrahmen, wenn „TF“ umgestellt ist); im höheren Zeitrahmen zählen nur abgeschlossene Kerzen (Signal erst nach Monats- bzw. Wochenschluss, kein Hin und Her innerhalb des Monats), aktuelle Position mit Einstieg,
  Ziel (3× ATR 14) und Stop (2× ATR 14, ATR im Zeitrahmen des Signals) als Linien, in der Kopfzeile MACD über/unter 0, Schwung steigt/fällt, letztes Signal mit Ziel/Stop in % und ein Check (wie oft Ziel vor Stop).
  Knopf „Ausstieg“: Ziel/Stop (wie oben) oder **Gegensignal** – Position halten bis zur Kreuzung in die andere Richtung (Ausstieg ohne Filter, auch wenn daraus kein neuer Einstieg wird; im Chart „EXIT ±x %“ bzw. „STOP“), Stop bleibt als Notbremse;
  der Check zeigt dann Anzahl, Ø Gewinn/Verlust je Signal in %, bestes und schlechtestes (offene Position zum aktuellen Kurs mitgezählt, ohne Gebühren).
  Knopf „Signale“: alle Kreuzungen / mit Trend (BUY nur bei MACD über null, SELL nur unter null; Wackler mit kleinem Histogramm davor zählen nicht) / nur Nulllinien-Durchgänge (wenigste Signale).
Nachgerechnet nach den bekannten Formeln, angelehnt an die TradingView-Indikatoren von LuxAlgo, ChrisMoody und blackcat (kein Originalcode).

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
