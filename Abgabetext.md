# Links
Webversion der Anwendung: https://kuehlfrank.de/  
Der Quellcode für dieses Projekt zugänglich unter: https://github.com/kuehlfrank  
Die für den Wettbewerb relevante Verion des Codes findet man unter: https://github.com/kuehlfrank/app/releases/tag/v1

## Anmerkungen:
Diese Lösung ist in Zusammenarbeit mit Alexander Korn, Nico Kranz, Lars Kecker, Linus Ricker und mir (Tom Stein) entstanden

# Übersicht 
Kühlfrank ist eine praktische Webanwendung um Empfehlungen zur Verwendung seiner Lebensmittel in Form von Rezeptvorschlägen zu erhalten. Die verwendung erfordert das erstellen eines Benutzerkontos (wir stellen weiter unter aber auch schon ein vorgefertigtes Benutzerkonto bereit). Als ersten Schritt muss der Nutzer seine vorhanden Lebensmittel erfassen. Dies geschieht entweder über die manuelle Eingabe oder die Barcode-Scanner funktion. Nach erfolgreicher Erfassung einiger Lebensmittel können die ersten Rezeptvorschläge eingesehen werden. Entscheidet der Benutzer sich eines der Rezepte zu kochen erfolgt automatisch eine Anpassung der Lagerbestände entsprechend der gewählten Portionsgröße.

## Test-Konto
Hier sind die Zugangsdaten für den oben erwähnten Test Account:  
E-Mail: `kuehlfrank@tomstein.me`  
Passwort: `XXXXXXXXXXXXXXXX`

# Technische Übersicht
Kühlfrank wurde als Webanwendung implementiert, um das Projekt Plattformunabhängig nutzen zu können.
Im Frontend verwendeten wir React mit Typescript während im Backend auf das Spring Framework in Java zurückgegriffen wurde. Unsere Postgres Datenbank wird mit hilfe von python (und rust) scripts befüllt.
Die Rezepte in der Datenbank wurden von der REWE- und EDEKA-Homepage übernommen.

Wichtig ist uns, dass das Projekt Kühlfrank in nahezu jedem Browser (insbesondere Mobile) ausführbar ist, weswegen wir u.a. css frameworks wie bootstrap verwendet haben. Durch die verwendung von React und damit Node.js war es uns sehr einfach möglich einen bereits halbwegs funktionierenden Barcode-Scanner zu implementieren.

## Starten der Anwendung
Neben der online Version unter [kuehlfrank.de](https://kuehlfrank.de/) ist es natürlich auch möglich die Anwendung lokal auszuführen. Dazu ist erstmal nur Docker notwendig (getestet auf Windows Hosts, sollte aber auch auf Linux funktionieren). Benötigt wird auch nur das [app repository](https://github.com/kuehlfrank/app), da in diesem die anderen repositories als git-submodule eingebunden sind. Entsprechende weitere Anweisungen zum Starten finden sich in der [Readme](https://github.com/kuehlfrank/app/blob/main/README.md#building-with-docker).  
Die einzelnen Teilprojekte können auch seperat gestartet werden. Insbesondere der Data-Scraper muss bei Bedarf seperat ausgeführt werden.

## Kurzer Abriss des Codes
Die Readmes der entsprechenden Teilprojekte geben bereits einen guten überblick, hier folt noch ein etwas detaillierter überblick.  
Readme zum Starten aller Container: https://github.com/ScholliYT/zf-optimize/blob/master/README.md

Seiten der https://github.com/ScholliYT/zf-optimize/tree/master/webapp/Pages
Models: https://github.com/ScholliYT/zf-optimize/tree/develop/webapp/Data/Entities
Frontend Guide: https://github.com/ScholliYT/zf-optimize/wiki/Frontend


# Verbesserungsvorschläge
Offenbar sind unsere Anfragen an den Teilnehmersupport im Datenstrom untergegangen. Für folgende Competitions würde schnellere Rückmeldung das Coden vereinfachen.
Ansonsten vielen Dank für die Competition.

# Vorschlag für folgende Competitions
Es wäre cool, wenn es mal eine Competition zum Thema "Cloud native" (Serverless Functions, Microservices, Event Queues usw.) geben würde. Vielleicht ja sogar mit gesponsorten Credits für Cloud-provider? Sonst gibts ja auch einige open-souce Möglichkeiten in diesem Rahmen.
