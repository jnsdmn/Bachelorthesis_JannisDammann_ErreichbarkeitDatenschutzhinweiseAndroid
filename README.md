# Bachelorthesis_JannisDammann_ErreichbarkeitDatenschutzhinweiseAndroid

ANLEITUNG ZUR INSTALLATION UND AUSFÜHRUNG DES PROGRAMMS
=======================================================

Schritt 1: Installation benötigter Software
-------------------------------------------
    1. Download und Installation von Android Studio (Link: https://developer.android.com/studio)
       => WICHTIG: Im Installationsprozess Haken sowohl bei Android Studio als auch bei Android Virtual Device setzen!
    (evtl. benötigt: JDK über https://www.oracle.com/java/technologies/javase-downloads.html)

Schritt 2: Vorbereitung für Ausführung
--------------------------------------
    1. Importieren des Projektes "bachelorthesisandroidproject" in Android Studio.

    2. Installation des Android-Emulators durch Android Studio:
        2.1 AVD Manager öffnen (4. Piktogramm von rechts in der Menüleiste oben rechts), ansonsten über: Help -> Find Action -> "AVD Manager" eingeben.
        2.2 Create Virtual Device anklicken.
        2.3 Bei Phone Pixel 2 auswählen (Dies wurde für die Arbeit benutzt, rein theoretisch kann jeder Emulator benutzt werden, der den Play Store beinhaltet).
        2.4 Als System Image Android "Q" (API Level 29, ABI x86, Android 10.0(Google Play)) herunterladen und auswählen.
        2.5 In der Konfiguration des Emulators "Show Advanced Settings" betätigen und den Speicher unter "Internal Storage" nach Belieben setzen (Bsp.: 4 GB).
        2.6 Bestätigen und Abschließen.

    3. Konfigurieren des Android Virtual Devices:
        3.1 AVD Manager benutzen, um Android Device zu starten.
        3.2 Mit Google Konto auf Gerät anmelden (Bspw. durch Öffnen des Play Stores).
        3.3 Deaktivieren der On-Screen-Tastatur: Settings -> System -> Languages & input -> Physical keyboard -> Show virtual keyboard (aus).

    4. Installation der zu testenden Anwendungen:
        4.1 Installation der Anwendungen durch den Play Store.
        4.2 Einmaliges Öffnen der jeweiligen Anwendungen, wenn nötig Anmeldung in den Anwendungen.
        4.3 Für jede Anwendung: Deaktivieren des Bild-in-Bild-Modus: Settings -> Apps & Notifications -> See all "" apps -> jeweilige App -> Advanced -> Picture-in-picture -> Deaktivieren.
        4.4 Alle zu testenden Anwendungen in einen Ordner auf dem Homescreen von Android hinterlegen (Name von Ordner muss lauten: "Tested Apps").

Schritt 3: Ausführen der Suche
------------------------------
    1. Lokalisieren der Testklasse: bachelorthesisandroidstudioproject -> app -> src -> androidTest -> java -> com.example.bachelorthesisandroidstudioproject -> DataPolicyRipper.java
    2. Ausführen der Testklasse durch Rechtsklick -> Run (auf dem Android Virtual Device)

Schritt 4: Anzeigen der Ergebnisse
----------------------------------
    1. Öffnen des LogCat von Android Studio: View -> Tool Windows -> Logcat
    2. Filter nach Ergebnissen einstellen: Im Logcat-Fenster rechts oben in Drop-Down-Menü Filter auswählen: "Edit Filter Configuration"
        2.1 Log Tag: Results
	2.2 Log Level: Error
    3. Ergebnisse seperat in ein externes Textdokument kopieren.

Schritt 5: Konvertieren der Ergebnisse durch Java-Programm
----------------------------------------------------------
    1. In der Zip-Datei des Programms ist ein seperat entwickeltes Programm mit dem Namen "Bachelorthesis_ResultConverter.jar" hinterlegt.
    2. Jar-Datei entpacken und öffnen.
    3. Importieren der Ergebnisse der Suche aus Textdokument(.txt): Convert File -> Open File -> Datei auswählen.
    4. Ergebnisse werden als Knotenpaare mit Häufigkeit angezeigt.
    5. Speichern der Ergebnisse in Textdokument: Save to File -> Dateiname und Speicherort auswählen.
    6. Der Quellcode des ResultConverter ist ebenfalls in der Abgabe enthalten.



ANMERKUNGEN ZUR ERGEBNISZUSAMMENFASSUNG IN DER EXCEL-DATEI
==========================================================
Die Ergebnisse aus der Analyse der Bachelorarbeit sind alle in der Excel-Datei "Gesamtergebnisse.xlsx" eingepflegt. In den Zeilen 1 bis 101 sind die 100 meistinstallierten Anwendungen
aus der Gesamtanalyse angegeben. Die Zeilen 112 bis 130 sind die Ergebnisse der Kontrollanwendungen von den Plätzen 482 bis 500. Die drei letzten Anwendungen in den Zeilen
140 bis 142 sind drei weitere Browseranwendungen, die für die Analyse der Browseranwendungen zusätzlich durchsucht wurden.
