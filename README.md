# PC’L Übersetzungen für FluentSMTP

Eine vollständige deutsche Übersetzung für **FluentSMTP**, in **Du und Sie** –
ausgeliefert als WordPress-Plugin, das seine Kataloge vor allen anderen lädt
und nebenbei die Datumsangaben der FluentSMTP-Verwaltung eindeutscht.

> Unabhängiges Projekt. Keine Verbindung zu WPManageNinja, den Herstellern von
> FluentSMTP.

> [!IMPORTANT]
> **Dieses Plugin wird nicht mehr gepflegt (Stand 22.09.2026).**
> Die deutsche Übersetzung für FluentSMTP liefert seit dem 22.09.2026
> **[pcl-fluent-de](https://github.com/blocoder/pcl-fluent-de)** aus – zusammen
> mit den Übersetzungen für FluentCommunity, FluentCommunity Pro,
> FluentMessaging, FluentPlayer, FluentAuth, FluentSMTP und FluentSnippets.
> Jede davon lässt sich dort einzeln abschalten oder auf Englisch stellen.
>
> **Die Releases dieses Repos sind entfernt**, hier gibt es nichts mehr zu
> installieren. Wer `pcl-fluentsmtp-de` noch aktiv hat: erst `pcl-fluent-de`
> einspielen, dann dieses Plugin deaktivieren. Solange es aktiv ist, hält sich
> der Nachfolger für FluentSMTP bewusst heraus, damit nicht zwei Kataloge und
> zwei gleichnamige Funktionen nebeneinander laden.
>
> Der Quellstand bleibt als Chronik stehen.

---

## Warum eine eigene deutsche Übersetzung?

FluentSMTP verschickt auf meinen WordPress-Seiten die Mails. Die deutsche
Übersetzung von wordpress.org deckt davon aber nur einen Teil ab: **342 von
827 Zeichenketten**, also rund 41 Prozent. Die Einstellungen, das
E-Mail-Protokoll und die Benachrichtigungen waren halb deutsch, halb englisch.

Dazu kommt: Das Sprachpaket gibt es **nur in der Du-Form** (`de_DE`).
WordPress weicht von `de_DE_formal` nicht auf `de_DE` aus. Auf einer Seite,
die siezt, bleibt FluentSMTP deshalb vollständig englisch.

Die Lösung ist dieselbe wie bei meiner Übersetzung für FluentCommunity
([pcl-fluent-de](https://github.com/blocoder/pcl-fluent-de)): **Wer zuerst
lädt, gewinnt.** Dieses Plugin lädt seine Kataloge auf `plugins_loaded` mit
Priorität 1, bevor FluentSMTP die erste Übersetzung anfordert. Die Kataloge
liegen im Plugin und wandern mit ihm von Installation zu Installation.

---

## Was drin ist

Stand: 17.09.2026, abgeglichen mit **FluentSMTP 2.4.0**.

| Katalog | Anrede | übersetzt | offen |
|---|---|---:|---:|
| `fluent-smtp-de_DE` | Du | 802 | 25 |
| `fluent-smtp-de_DE_formal` | Sie | 802 | 25 |

**Die 25 offenen Einträge sind Absicht:** Produkt- und Anbieternamen (Amazon
SES, Mailgun, Postmark, Telegram …), die Kürzel `HTML`, `SSL` und `TLS`,
`PHP mail()`, ein Menüpfad aus der Cloudflare-Oberfläche, die Adresse und die
Autorenzeile des Herstellers, eine Beispieladresse und der Befehl, den man an
den Telegram-Bot von FluentSMTP schickt – übersetzt würde der Bot ihn nicht
mehr verstehen. Jeder offene Eintrag trägt einen Übersetzerkommentar mit dem
Grund.

Ein Katalog gehört zu einer Plugin-Version. Ändert der Hersteller einen
englischen Text, ist das für gettext ein neuer Schlüssel, und der alte fällt
aus dem Katalog. Auf einer älteren FluentSMTP-Version können einzelne
Zeichenketten deshalb englisch erscheinen. Am besten erst FluentSMTP
aktualisieren, dann dieses Plugin.

---

## Wie übersetzt wurde

**Du ist die Leitfassung, Sie wird daraus abgeleitet.** Welche Fassung
greift, entscheidet die Sprache der Seite (`de_DE` oder `de_DE_formal`).
Die Texte sind weitgehend ohne Anrede formuliert („Bitte einen Anbieter
auswählen“ statt „Bitte wähle einen Anbieter aus“). Du und Sie unterscheiden
sich deshalb nur in zwölf Einträgen: den Schritt-für-Schritt-Anleitungen für
toSend und Cloudflare.

**Ein eigenes Glossar sorgt für Konsistenz.** Ein paar Beispiele:

| Englisch | Deutsch |
|---|---|
| Connection | Verbindung |
| Default / Fallback Connection | Standardverbindung / Ausweichverbindung |
| From Email / From Name | Absenderadresse / Absendername |
| Email Logs | E-Mail-Protokoll |
| Alerts, Notifications | Benachrichtigungen |
| Email Summary | E-Mail-Zusammenfassung |
| Credentials | Zugangsdaten |
| API Key / Access Key / Secret Key | API-Schlüssel / Zugriffsschlüssel / geheimer Schlüssel |

**Anbieterbegriffe folgen dem Anbieter.** Bei Microsoft Entra heißt es
„Umleitungs-URIs“ und „Verzeichnis-ID (Mandant)“, bei Google Cloud
„Autorisierte Weiterleitungs-URIs“ – so, wie es in deren deutscher Oberfläche
steht, damit man die Stelle dort wiederfindet.

**Satzbausteine sind im Zusammenhang übersetzt.** Viele Hinweise setzt
FluentSMTP aus Stücken zusammen: Satzanfang, Link, Satzende. Jedes Stück ist
gegen die Stelle geprüft, an der es in der Oberfläche landet.

Dazu die Hausregeln: typografische Anführungszeichen `„…“`, ein echtes
Auslassungszeichen `…` statt drei Punkten, keine Ausrufezeichen, keine Emojis.

---

## Was das Plugin außerdem tut

**Es hält das Sprachpaket von wordpress.org fern.** Als Lückenfüller ergäbe es
eine Oberfläche aus zwei Übersetzungen mit unterschiedlichen Begriffen, und
eine bewusst englische Stelle soll englisch bleiben. Wer das Paket trotzdem
dahinter haben will:

```php
add_filter( 'pcl_fluentsmtp_de/keep_foreign_german', '__return_true' );
```

**Es stellt die Datumsangaben der Verwaltung auf Deutsch.** FluentSMTP
formatiert Daten im Browser ohne Sprache. Mit dem Plugin steht im
E-Mail-Protokoll „16. Sep. 2026, 18:17“ statt „16 Sep 2026 6:17 PM“ und an der
Versandstatistik „11. Sep.“ statt „Sep 11“. Datumswähler und Seitennavigation
werden ebenfalls deutsch („Mo … So“, die Woche beginnt am Montag, „Gesamt: 27“,
„10/Seite“), und Datumsbereiche trennt ein Pfeil: „Startdatum → Enddatum“.
Das wirkt nur auf der FluentSMTP-Seite im Backend und nur bei deutscher
Sprache. Abschalten:

```php
add_filter( 'pcl_fluentsmtp_de/dayjs_deutsch', '__return_false' );
```

Zwei Dinge bleiben, wie sie sind: Der Kopf des Datumswählers lautet
„2026 September“ (die Reihenfolge ist in der Bibliothek fest), und die Werte
im Datumsfeld bleiben im ISO-Format, weil FluentSMTP genau dieses Format an den
Server schickt.

**Es übersetzt auch nach einem Sprachwechsel.** Wechselt WordPress mitten in
einem Aufruf die Sprache (`switch_to_locale()`, etwa wenn ein anderes Plugin
eine Mail in der Sprache des Empfängers baut), lädt das Plugin seine Kataloge
für die neue Sprache nach. Ohne das fiele FluentSMTP an dieser Stelle auf
Englisch zurück.

Welche Kataloge das Plugin lädt, lässt sich über einen Filter anpassen:

```php
add_filter( 'pcl_fluentsmtp_de/domains', function ( $domains ) { … } );
```

---

## Installation

1. Das ZIP aus [Releases](https://github.com/blocoder/pcl-fsmtp-de/releases)
   herunterladen.
2. Im Backend unter *Plugins → Installieren → Plugin hochladen* einspielen und
   aktivieren.

Das ZIP steht unter *Releases* am rechten Rand der Repo-Startseite. Der grüne
Knopf *Code → Download ZIP* daneben liefert den Quellcode ohne die gebauten
Kataloge und damit ein Plugin, das nichts übersetzt.

Die Seite muss auf `de_DE` oder `de_DE_formal` stehen. In der Plugin-Liste
steht danach, welcher Katalog tatsächlich greift. Weitere Updates meldet das
Plugin von selbst und holt sie von hier.

Der Plugin-Ordner heißt `pcl-fluentsmtp-de`, auch wenn das Repo kürzer heißt.

**Voraussetzungen:** WordPress 6.5+, PHP 7.4+, FluentSMTP.

---

## Mitmachen

Ein Wort, das nicht passt? Eine Zeichenkette, die im Zusammenhang falsch
klingt? [Ein Issue](https://github.com/blocoder/pcl-fsmtp-de/issues) mit dem
englischen Original und der Stelle, an der es auftaucht, hilft am meisten.

Die `.po`-Dateien liegen in `languages/` und lassen sich direkt bearbeiten –
auch mit Loco Translate im Backend, dafür ist die `loco.xml` da. Die
kompilierten `.mo`- und `.l10n.php`-Dateien stehen nur im Release-Archiv,
nicht im Repo: Sie sind Erzeugnisse.

Was sich an FluentSMTP selbst nicht übersetzen lässt, ist beim Hersteller
gemeldet: [WPManageNinja/fluent-smtp#430](https://github.com/WPManageNinja/fluent-smtp/issues/430).

---

## Lizenz

`GPL-2.0-or-later`, siehe [LICENSE](LICENSE).

Die Kataloge enthalten die Quellzeichenketten von FluentSMTP und sind damit
abgeleitete Werke GPL-lizenzierter Software. Nutzung, Änderung und Weitergabe
sind erlaubt, kommerziell eingeschlossen.

Mitgeliefert ist die Bibliothek
[plugin-update-checker](https://github.com/YahnisElsts/plugin-update-checker)
von Jānis Elsts (MIT-Lizenz, siehe `plugin-update-checker/license.txt`).

Namensnennung freut mich, ist aber keine Bedingung.
