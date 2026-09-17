# Änderungen

Die Versionsnummer steigt bei **jeder** Katalogänderung, auch wenn sich am
Plugin-Code nichts tut. Ein Archiv, dessen Name nichts über seinen Inhalt
sagt, ist beim Weitergeben wertlos.

Frühere Fassungen liefen nicht öffentlich; diese Liste beginnt mit dem ersten
veröffentlichten Stand.

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
