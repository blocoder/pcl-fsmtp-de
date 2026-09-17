=== PC'L Übersetzungen für FluentSMTP ===
Contributors: blocoder
Tags: fluentsmtp, smtp, deutsch, übersetzung, german
Requires at least: 6.5
Tested up to: 7.1
Requires PHP: 7.4
Stable tag: 1.3.0
License: GPL-2.0-or-later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Eine vollständige deutsche Übersetzung für FluentSMTP, in Du und Sie – samt deutscher Datumsangaben in der Verwaltung.

== Description ==

802 übersetzte Zeichenketten für FluentSMTP 2.4.0, ausgeliefert als eigenes Plugin, in zwei Anreden: `de_DE` (Du) und `de_DE_formal` (Sie).

**Warum das nötig ist:** Das Sprachpaket von wordpress.org übersetzt weniger als die Hälfte der Oberfläche und gibt es nur in der Du-Form. Auf einer Seite mit `de_DE_formal` bleibt FluentSMTP damit ganz englisch.

**Was das Plugin sonst noch tut:** Datumsangaben im E-Mail-Protokoll und in der Versandstatistik erscheinen deutsch („16. Sep. 2026, 18:17“), ebenso Datumswähler und Seitennavigation. Datumsbereiche trennt ein Pfeil.

Unabhängiges Projekt, keine Verbindung zu WPManageNinja.

== Installation ==

1. Das ZIP aus den GitHub-Releases herunterladen.
2. Im Backend unter Plugins → Installieren → Plugin hochladen einspielen und aktivieren.

Die Seite muss auf `de_DE` oder `de_DE_formal` stehen. Weitere Updates meldet das Plugin von selbst.

== Frequently Asked Questions ==

= Muss ich das offizielle Sprachpaket entfernen? =

Nein. Das Plugin lädt es gar nicht erst, solange es aktiv ist. Wer es als Lückenfüller behalten will, setzt den Filter `pcl_fluentsmtp_de/keep_foreign_german` auf `true`.

= Wird das Paket auf Echtheit geprüft? =

Nein. WordPress bringt dafür einen Rahmen mit, wendet ihn aber nur auf Downloads von wordpress.org an. Was das Paket schützt, ist HTTPS und GitHub.

= Warum erscheinen einzelne Texte englisch? =

Ein Katalog gehört zu einer Plugin-Version. Ändert der Hersteller einen englischen Text, ist das für gettext ein neuer Schlüssel. Am besten erst FluentSMTP aktualisieren, dann dieses Plugin. Produktnamen und technische Bezeichner bleiben bewusst englisch.

== Changelog ==

= 1.3.0 =
* Erste öffentliche Fassung, abgeglichen mit FluentSMTP 2.4.0.
* Das Plugin meldet Updates jetzt selbst und holt sie von GitHub.
