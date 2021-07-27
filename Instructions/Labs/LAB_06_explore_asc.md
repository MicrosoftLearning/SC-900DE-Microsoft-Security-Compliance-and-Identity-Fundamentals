---
lab:
    title: 'Erkunden von Azure Security Center'
    module: 'Modul 3, Lektion 2: Beschreiben der Funktionen der Microsoft-Sicherheitslösungen: Beschreiben der Sicherheitsverwaltungsfunktionen von Azure'
---


# Lab: Erkunden von Azure Security Center 

## Labszenario
In diesem Lab erkunden Sie Azure Security Center und erfahren, wie Sie mithilfe der Azure-Sicherheitsbewertung den Sicherheitsstatus Ihrer Organisation verbessern können.

  

**Geschätzte Dauer**: 10–15 Minuten

#### Aufgabe 1: Bei dieser Aufgabe erhalten Sie eine Schnelleinführung in Azure Security Center.
1.	Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

1. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden** aus.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

1. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann **Alle Dienste** aus.  
1. Geben Sie **Security Center** in das Feld „Dienste filtern“ ein. Wählen Sie dann aus der Liste mit den Ergebnissen den Eintrag **Security Center** aus.
1. Beachten Sie die auf der Übersichtsseite von Security Center verfügbaren Informationen.  
1. Möglicherweise wird oben auf der Seite ein blaues Informationsfeld angezeigt, das darauf hinweist, dass Sie möglicherweise nicht alle Informationen sehen.  Wählen Sie **Hier klicken** aus.
    1. Weisen Sie sich selbst die erforderliche Roll zu, um sicherzustellen, dass Sie über die mandantenweite Sichtbarkeit verfügen.  Wählen Sie **Sicherheitsadministrator** aus. Wählen Sie dann unten auf der Seite **Zugriff anfordern** aus.
   
     1. Wahrscheinlich wird die Meldung „Stammverwaltungsgruppe ist nicht vorhanden“ angezeigt.  Laut Beschreibung wird die Gruppe vom System für Sie erstellt.  Dieser Vorgang kann bis zu 15 Minuten dauern (ist in der Regel aber schneller). Danach können Sie den Prozess wiederholen, um Zugriff zu erhalten.  Sobald der Zugriff erteilt wurde, wählen Sie in der oberen linken Ecke der Seite oberhalb von „Berechtigungen abrufen“ die Option **Security Center** aus, und aktualisieren Sie dann die Security Center-Übersichtsseite.
1. Oben auf der Seite finden Sie Informationen wie die Anzahl der Azure-Abonnements, die Anzahl der bewerteten Ressourcen, die Anzahl der aktiven Empfehlungen und alle Sicherheitswarnungen.  In der Mitte der Seite befinden sich Karten für die Sicherheitsbewertung, die Einhaltung gesetzlicher Bestimmungen, Insights, Azure Defender und mehr.  
1. Wählen Sie oben auf der Seite die Option **Bewertete Ressourcen** aus.  Dadurch gelangen Sie zur Seite „Inventar“, auf der Ihr Azure Pass-Abonnement angezeigt wird.  Wählen Sie **Azure Pass-Förderung** aus.
1. Auf der Seite „Resource Health“ finden Sie eine Liste mit Empfehlungen.  Wählen Sie in der verfügbaren Liste die Option **Ihrem Abonnement sollte mehr als ein Besitzer zugewiesen sein** aus. 
1. Wählen Sie den Dropdownpfeil neben den Wartungsschritten aus. Beachten Sie, dass ausführliche Schritte zur Wartung sowie eine entsprechende Option für Gegenmaßnahmen angezeigt werden.  
1. Wählen Sie oben links auf dem Bildschirm **Security Center** aus, um zur Übersichtsseite von Security Center zurückzukehren.
1. Wählen Sie oben auf der Seite die Option **Aktive Empfehlungen** aus.  
1. Auf der Seite mit den Empfehlungen werden bestimmte Aktionen angezeigt, die bei einem potenziellen Anstieg der Sicherheitsbewertung vorgenommen werden können.  Schließen Sie die Empfehlungsseite mit dem **X** oben rechts auf dem Bildschirm.
1. Wählen Sie auf der Hauptseite **Einhaltung gesetzlicher Bestimmungen** aus.
1. Auf der Seite „Einhaltung gesetzlicher Bestimmungen“ finden Sie eine Liste mit Compliancekontrollen.  Unter jeder Kontrolle befinden sich eine Reihe von Bewertungen, die auf dem Azure-Sicherheitsvergleichstest basieren. Dieser liefert Empfehlungen dazu, wie Sie Ihre Cloudlösungen auf Azure schützen können.
1. Wählen Sie **IM** aus.** Identitätsverwaltung** und dann **IM.4 Verwenden stärkerer Authentifizierungssteuerungen für den gesamten Azure Active Directory-basierten Zugriff** aus.  In der Liste werden Aktionen zur Verbesserung der Compliancesituation aufgeführt, für die der Kunde verantwortlich ist.
1. Wählen Sie das **X** oben rechts auf dem Bildschirm aus, um die Seite zu schließen und zur Übersichtsseite von Security Center zurückzukehren. 
1. Lassen Sie die Übersichtsseite von Security Center geöffnet. Sie werden sie bei der nächsten Aufgabe verwenden.


#### Aufgabe 2: Bei dieser Aufgabe navigieren Sie zur Azure-Sicherheitsbewertung und erkunden Empfehlungen, die Ihre Sicherheitsbewertung verbessern können. 

1. Wählen Sie auf der Übersichtsseite von Security Center die Karte **Sicherheitsbewertung** aus.

2. Wählen Sie **Azure Pass-Förderung** aus.  Beachten Sie Ihre Sicherheitsbewertung.
3. Wählen Sie auf der Empfehlungsseite die Option **Zugriff und Berechtigungen verwalten** aus. Beachten Sie, dass in dieser Gruppe ein Element rot ist.
4. Wählen Sie das Element **Ihrem Abonnement muss mehr als ein Besitzer zugewiesen sein** aus, das den Ressourcenintegritätsstatus in Rot anzeigt. Bei dieser Auswahl ist es nicht möglich, dieses Element auszuwählen.
    1. Wählen Sie in der oberen linken Ecke der Seite oberhalb von „Empfehlungen“ die Option **Security Center** aus.
    
    1. Wählen Sie im linken Navigationsbereich **Empfehlungen** aus.
    1. Wählen Sie auf der Empfehlungsseite die Option **Zugriff und Berechtigungen verwalten** aus. Beachten Sie, dass in dieser Gruppe ein Element rot ist.
    1. Wählen Sie das Element **Ihrem Abonnement muss mehr als ein Besitzer zugewiesen sein** aus, das den Ressourcenintegritätsstatus in Rot anzeigt. 
5. Wählen Sie das **Azure-Abonnement** aus.
6. Wählen Sie oben auf der Seite „Zugriffssteuerung (IAM)“ die Option **+ Hinzufügen** aus. Wählen Sie dann aus dem Dropdown den Eintrag **Rollenzuweisung hinzufügen** aus.
7. Geben Sie in das Feld „Rolle“ den Text **Besitzer** ein, und wählen Sie dann **Besitzer** aus der Liste darunter aus.
8. Wählen Sie **Alex Wilber** aus der Benutzerliste aus. Wählen Sie dann unten auf der Seite **Speichern** aus.
9. Es kann bis zu 24 Stunden dauern, bis der Status aktualisiert wird. Danach wird auch Ihre Sicherheitsbewertung aktualisiert, da alle Elemente in der Gruppe „Zugriff und Berechtigungen verwalten“ erfüllt sind.
10. Wählen Sie in der oberen linken Ecke der Seite oberhalb von „Azure Pass“ die Option **Security Center** aus. Wählen Sie dann **Übersicht** aus, um zur Übersichtsseite von Security Center zurückzukehren.
11. Lassen Sie diese Seite für die nachfolgende Aufgabe geöffnet.


#### Aufgabe 3:  Beachten Sie, dass Security Center in zwei Modi angeboten wird: „Azure Defender AUS“ (kostenlos) und „Azure Defender EIN“. Bei dieser Aufgabe erkunden Sie, wie Sie Azure Defender aktivieren und deaktivieren.

1.	Wählen Sie auf der Übersichtsseite von Security Center auf der Karte „Azure Defender“ die Option **Azure Defender aktivieren** aus.

2.	Wählen Sie das Feld **Azure Defender EIN** aus.  Beachten Sie, wie der Status sämtlicher Defender-Pläne in „EIN“ geändert wird, und beachten Sie die Preise für jedes Element. Wählen Sie dann in der oberen linken Ecke der Seite **Speichern** aus.
3.	Kehren Sie zur Seite „Security Center“ zurück, indem Sie in der oberen linken Ecke der Seite **Security Center** auswählen.   Es kann ein paar Minuten dauern, bis die Änderung auf der Karte „Azure Defender“ angezeigt wird.  Aktualisieren Sie die Seite bei Bedarf.
4.	Wählen Sie zum Deaktivieren von Azure Defender im linken Navigationsbereich der Seite „Security Center“ die Option **Preise und Einstellungen** aus. Wählen Sie anschließend **Abonnement für Azure Pass-Förderung** aus.
5.	Wählen Sie auf der Seite für Azure Defender-Pläne das Feld **Azure Defender AUS** aus. Wählen Sie dann in der oberen linken Ecke der Seite **Speichern** aus.
6.	Ein Popupfenster wird angezeigt. Darin werden Sie aufgefordert, das Downgrade zu bestätigen.  Deaktivieren Sie das Kästchen, dass sich Microsoft mit Ihnen in Verbindung setzen darf, und wählen Sie **Bestätigen** aus.
7.	Sie können nun die Browserregisterkarte schließen, um das Azure-Portal zu beenden.


#### Überprüfung
In diesem Lab haben Sie Azure Security Center erkundet und erfahren, wie Sie mithilfe der Azure-Sicherheitsbewertung den Sicherheitsstatus Ihrer Organisation verbessern können.
