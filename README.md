# files2gramps
Java lib for files to pack as a export into gramps database format.

[![Build Status](https://travis-ci.org/FunThomas424242/releasebuild.example.svg?branch=master)](https://travis-ci.org/FunThomas424242/releasebuild.example)
[![codecov](https://codecov.io/gh/FunThomas424242/releasebuild.example/branch/master/graph/badge.svg)](https://codecov.io/gh/FunThomas424242/releasebuild.example)
[![Download](https://api.bintray.com/packages/funthomas424242/funthomas424242-maven-plugins/releasebuild.example/images/download.svg) ](https://bintray.com/funthomas424242/funthomas424242-maven-plugins/releasebuild.example/_latestVersion)


# Usage
```
java -jar target/releasebuild.example-0.0.0-SNAPSHOT-jar-with-dependencies.jar
or
mvn exec:java
```
# Beschreibung - Releasebau
1. Projekt aufsetzen
2. branch production erstellen
3. branch feature/xxx erstellen
4. feature auf feature branch implementieren
5. feature in den master mergen
6. release auf dem master bauen
7. release tag in den production branch mergen
8. production branch deployen

# Fallen
1. Beim Bilden des Release 0.0.0 wurde einfach mvn release:prepare und mvn release:perform ausgeführt
* Prepare wurde interaktiv durchgeführt und es wurde ein push des release Tags ausgelöst. Leider enthält 
der Tag release.example-0.0.0 eine pom.xml mit SNAPSHOT Version. Das hätte ich nicht erwartet.
* Das Perform wurde abgebrochen weil das Deployment auf Grund ungültiger Zugangsdaten scheiterte. Es
entstand eine Situation die ich nicht mehr lösen konnte. Ich entschied mich das Release zu canceln und 0.0.1 vorzubereiten.
Dazu spaltete ich den Branch feature/vorgehen2 ab. Die pom.xml steht auf 0.0.1-SNAPSHOT

