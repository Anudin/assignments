# Assignment 6: Ein Butler für Sie

**Obacht** - Sie erreichen unseren Jenkins unter `http://141.19.142.63:**8081**`.

## Installation
* Installation von Jenkins über apt
* Installation von Java 14 über apt, benötigt für Maven Builds
	* Achtung: Java 11 muss ebenfalls installiert **und im PATH eingetragen sein** - sonst startet Jenkins nicht
* Jenkins öffnen auf `localhost:8080`, Nutzer anlegen

## Jenkins Konfiguration
* Plugin Installation über integrierte Verwaltung: *Maven Integration plugin*
* In Jenkins: Eintragen Java 14 bei "Konfiguration der Hilfsprogramme"
* CSS Fix für Reports über JAVA_ARGS in /etc/default/jenkins
* SSH Zugang einrichten (in GitHub & Jenkins)

## Tomcat Maven-Projekt Build
* Projekt anlegen & konfigurieren
	* Build Trigger mit *Poll SCM*
	* Stamm-POM eintragen
	* Goals eintragen
	* Shell-Skript anlegen um Artefakte zu packen (tgz Format)
	* tgz als Post-Build-Aktion archivieren lassen

## Pipeline Build
