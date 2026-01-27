# Inhalt
- *maven-dep-resolver* ist das Maven Plugin zum analysieren der Dependencies
- *proguard-maven-plugin* ist das Test Maven Plugin zum analysieren der Dependencies [https://github.com/wvengen/proguard-maven-plugin](https://github.com/wvengen/proguard-maven-plugin)
- *maven-dep-plugin-1.0-SNAPSHOT.zip* ZIP des IntelliJ zum lokalen installieren in IntelliJ

# Installationsanleitung

Diese Anleitung beschreibt die notwendigen Schritte zur Installation der benötigten Software für dieses Projekt.

## Voraussetzungen

### 1. Java 25
Stellen Sie sicher, dass Java 25 (JDK) auf Ihrem System installiert ist.


### 2. Maven
Maven wird zur Verwaltung der Projektabhängigkeiten und zum Bauen des Projekts benötigt.
- Laden Sie Maven von [maven.apache.org](https://maven.apache.org/download.cgi) herunter.


### 3. IntelliJ IDEA
- Da das Interface als Plugin für IntelliJ entwickelt wurde, muss IntelliJ IDEA installiert sein.

### 4. Graphviz (dot)
Das Tool `dot` ist Teil von Graphviz und wird zur Visualisierung von Abhängigkeitsgraphen benötigt.
- Laden Sie Graphviz von [graphviz.org](https://graphviz.org/download/) herunter.
- Stellen Sie sicher, dass das Verzeichnis mit der `dot.exe` (meistens im `bin`-Ordner von Graphviz) in Ihrem System-`PATH` enthalten ist.
- Überprüfung: `dot -V`.

## Installation

### 1. IntelliJ Plugin installieren
Das IntelliJ Plugin wird manuell aus einer ZIP-Datei installiert:
- Öffnen Sie IntelliJ IDEA.
- Gehen Sie zu `File` -> `Settings` (unter macOS `IntelliJ IDEA` -> `Settings`).
- Wählen Sie `Plugins`.
- Klicken Sie auf das Zahnrad-Symbol (oder "Install Plugin from Disk...") und wählen Sie `Install Plugin from Disk...`.
- Wählen Sie die Datei `maven-dep-plugin-1.0-SNAPSHOT.zip` im Projektverzeichnis aus.

### 2. Maven Plugin installieren
- Navigieren Sie im Terminal in das Verzeichnis `maven-dep-resolver`
- Führen Sie den Befehl `mvn install` aus

### 3. proguard-maven-plugin
- Navigieren Sie im Terminal in das Verzeichnis `proguard-maven-plugin`
- Führen Sie den Befehl `mvn package` aus

### 4. IntelliJ Plugin Interface
- Öffnen sie das proguard Projekt einzeln und führen sie "load data" aus
- Nun sollten die Informationen zur verfügung stehen
