# Änderungen

Die Versionsnummer steigt bei **jeder** Katalogänderung, auch wenn sich am
Plugin-Code nichts tut. Ein Archiv, dessen Name nichts über seinen Inhalt
sagt, ist beim Weitergeben wertlos.

Frühere Fassungen liefen nicht öffentlich; diese Liste beginnt mit dem ersten
veröffentlichten Stand.

## 1.3.2

**Dieses Plugin wird eingestellt.** Die Übersetzung für FluentSMTP liegt seit dem
22.09.2026 in „PC’L Übersetzungen für Fluent-Plugins“ (`pcl-fluent-de`),
zusammen mit denen für FluentCommunity, FluentMessaging, FluentPlayer und die
beiden anderen Schwester-Plugins. Dort lässt sich jede Übersetzung einzeln
abschalten oder ganz auf Englisch stellen, und ein Katalog wird nur noch
gelesen, wenn sein Plugin installiert ist.

**Was zu tun ist:** [pcl-fluent-de installieren][nachfolger], danach dieses
Plugin deaktivieren und löschen. Solange beide aktiv sind, hält sich das neue
Plugin für diese Textdomain heraus – es geht also nichts kaputt, wenn die
Umstellung ein paar Tage dauert.

Am Code ändert sich mit dieser Fassung nichts. Wer hier bleibt, behält den
Katalog vom 22.09.2026; neue Zeichenketten kommen nur noch drüben an.

[nachfolger]: https://github.com/blocoder/pcl-fluent-de/releases

## 1.3.1

**Ein Hinweis, wenn die gebauten Kataloge fehlen.** Wer das Plugin aus dem
Quellcode-Archiv von GitHub installiert („Code → Download ZIP“) statt aus den
Releases, bekommt nur die `.po`-Dateien und damit ein Plugin, das nichts
übersetzt. Von außen war das nicht zu erkennen – die Plugin-Liste meldete
lediglich „Keine Kataloge gefunden“, was nach einem Problem mit der Sprache
aussieht. Jetzt benennt das Plugin die Ursache, in der Plugin-Liste und als
Hinweis in der Verwaltung, samt Link auf das richtige Archiv.

An den Katalogen ändert sich nichts.

## 1.3.0

**Erste öffentliche Fassung**, abgeglichen mit FluentSMTP 2.4.0.

- Deutsche Übersetzung in Du (`de_DE`) und Sie (`de_DE_formal`): 802 von 827
  Zeichenketten, die übrigen 25 bleiben mit Begründung englisch.
- Das Sprachpaket von wordpress.org wird nicht geladen, solange das Plugin
  aktiv ist (abschaltbar über `pcl_fluentsmtp_de/keep_foreign_german`).
- Datumsangaben in E-Mail-Protokoll, letzten Aktivitäten und Versandstatistik
  erscheinen deutsch („16. Sep. 2026, 18:17“, „11. Sep.“).
- Datumswähler und Seitennavigation sind deutsch („Mo … So“, Woche ab Montag,
  „Gesamt: 27“, „10/Seite“); Datumsbereiche trennt ein Pfeil.
- Das Plugin meldet Updates selbst und holt sie aus den Releases dieses Repos.
