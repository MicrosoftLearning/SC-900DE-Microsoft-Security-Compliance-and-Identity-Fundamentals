﻿---
lab:
    title: 'Erkunden von Azure Sentinel'
    module: 'Modul 3, Lektion 3: Beschreiben der Funktionen der Microsoft-Sicherheitslösungen: Beschreiben der Sicherheitsfunktionen von Azure Sentinel'
---


# Lab: Erkunden von Azure Sentinel 

## Labszenario
In diesem Lab gehen Sie den Prozess der Erstellung einer Azure Sentinel-Instanz durch.  Zudem richten Sie die Berechtigungen ein, um den Zugriff auf die Ressourcen sicherzustellen, die zur Unterstützung von Azure Sentinel bereitgestellt werden.  Nach Abschluss dieser grundlegenden Einrichtung gehen Sie die Schritte zum Herstellen eine Verbindung von Sentinel mit Ihren Datenquellen durch. Sie verwenden dabei integrierte Analysen, um über verdächtige Aktivitäten benachrichtigt zu werden. Als Letztes erkunden Sie die Automatisierungsfunktion.  

  

**Geschätzte Dauer**: 30–45 Minuten

#### Aufgabe 1:  Erstellen einer Azure Sentinel-Instanz

1. Öffnen Sie Microsoft Edge. Geben Sie **portal.azure.com** in die Adressleiste ein.

2. Melden Sie sich mit Ihren Administratoranmeldeinformationen an.
    1. Geben Sie **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ ist hierbei die eindeutige Mandanten-ID, die von Ihrem Labhostinganbieter bereitgestellt wurde) in das Fenster „Anmelden“ ein, und wählen Sie dann **Weiter** aus.
    
    1. Geben Sie das Administratorkennwort ein, das Sie vom Labhostinganbieter erhalten haben sollten. Wählen Sie **Anmelden** aus.
    1. Wählen Sie **Ja** aus, wenn Sie gefragt werden, ob Sie angemeldet bleiben möchten.

3. Wählen Sie in der oberen linken Ecke des Bildschirms neben dem Text „Microsoft Azure“ das Symbol „Portalmenü anzeigen“ (die drei horizontalen Linien werden auch als Hamburgersymbol bezeichnet) und dann **Alle Dienste** aus.  

4. Geben Sie **Sentinel** in das Feld „Dienste filtern“ ein. Wählen Sie dann **Azure Sentinel** aus der Liste aus.

5. Wählen Sie auf der Seite „Azure Sentinel“ die Option **Azure Sentinel erstellen** aus.

6. Wählen Sie auf der Seite „Azure Sentinel hinzufügen“ die Option **Neuen Arbeitsbereich erstellen** aus.

7. Geben Sie auf der Registerkarte „Grundlagen“ von „Log Analytics-Arbeitsbereich erstellen“ Folgendes ein:
    1. Abonnement:  **Azure Pass-Förderung**
   
    1. Ressourcengruppe: Wählen Sie **Neu erstellen** aus, geben Sie dann den Namen **SC900-ResourceGroup** ein, und wählen Sie **OK** aus.
    1. Name: **SC900-LogAnalytics-workspace**.
    1. Region: **East US** (übernehmen Sie diesen Standardwert).
    1. Wählen Sie **Weiter: „Tarif >“ aus.**

8. Übernehmen Sie für „Tarif“ die Standardeinstellungen: **Nutzungsbasierte Bezahlung (Pro GB 2018)**. Wählen Sie dann **Weiter: Tags >** aus.

9. Für „Tags“ können Sie dies leer lassen. Wählen Sie dann **Bewerten + erstellen** aus.

10. Überprüfen Sie Ihre eingegebenen Informationen, und wählen Sie dann **Erstellen** aus.

11. Wenn der neue Arbeitsbereich nicht aufgelistet wird, wählen Sie **Aktualisieren** und dann **Hinzufügen** aus.

12. Nachdem der neue Arbeitsbereich hinzugefügt wurde, wird die Seite „News und Anleitungen zu Azure Sentinel“ | angezeigt.  Beachten Sie die drei auf der Seite „Erste Schritte“ aufgelisteten Schritte.

13. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Aufgabe 2:  Nachdem Sie die Azure Sentinel-Instanz erstellt haben, möchten Sie sicherstellen, dass Sie über den erforderlichen Zugriff auf die Ressourcen verfügen, die zum Unterstützen von Azure Sentinel bereitgestellt werden.  Bei dieser Aufgabe navigieren Sie zur Seite „Zugriffssteuerung (IAM)“ für die von Ihnen mit der Azure Sentinel-Instanz erstellten Ressourcengruppe, zeigen die verfügbaren Rollen an und weisen sich selbst (MOD-Administrator) die erforderliche Rolle zu. Durch das Zuweisen der Rolle auf der Ressourcengruppenebene wird sichergestellt, dass die Rolle für alle Ressourcen gilt, die zum Unterstützen von Azure Sentinel bereitgestellt werden.

1. Wählen Sie auf der Seite „Azure Sentinel“ in der oberen linken Ecke der Seite oberhalb des Texts „Azure Sentinel“ die Option **Alle Dienste** aus.

2. Geben Sie die Ressourcengruppen in das Feld „Dienste filtern“ ein. Wählen Sie dann in der bereitgestellten Liste den Eintrag **Ressourcengruppen** aus.

3. Wählen Sie auf der Seite „Ressourcengruppen“ die von Ihnen mit Azure Sentinel erstellte Ressourcengruppe aus, nämlich **SC900-ResourceGroup**.

4. Wählen Sie auf der Seite „SC900-ResourceGroup“ im linken Navigationsbereich die Option **Zugriffssteuerung (IAM)** aus.

5. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **Meinen Zugriff anzeigen** aus.  Beachten Sie, dass die aktuelle Rolle „Sicherheitsadministrator“ lautet.  Wählen Sie zum Schließen des Fensters für die MOD-Administratorzuweisungen das **X** aus, das sich in der oberen rechten Ecke des Fensters befindet.

6. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **+ Hinzufügen** und dann **Rollenzuweisung hinzufügen** aus.

7. Das Fenster „Rollenzuweisung hinzufügen“ wird geöffnet.  Wählen Sie den Dropdownpfeil im Feld „Rolle auswählen“ aus, um die verfügbaren Rollen anzuzeigen.  Wählen Sie für dieses Lab **Besitzer** aus.  HINWEIS:  Als bewährte Methode empfiehlt es sich, die niedrigste Berechtigung zuzuweisen, die für die Rolle erforderlich ist.  Überprüfen Sie als Referenz die Berechtigungen in Azure Sentinel:  https://docs.microsoft.com/de-de/azure/sentinel/roles

8. Wählen Sie in der angezeigten Liste der Benutzer den Eintrag **MOD-Administrator** aus.

9. Wählen Sie unten auf der Seite **Speichern** aus.

10. Wählen Sie auf der Seite „Zugriffssteuerung“ die Option **Meinen Zugriff anzeigen** aus, um zu bestätigen, dass die Rolle hinzugefügt wurde. Schließen Sie dann das Fenster, indem Sie in der oberen rechten Ecke des Fensters das **X** auswählen.

11. Kehren Sie zur Seite „Alle Dienste“ von Azure zurück. Wählen Sie dazu in der oberen linken Ecke der Seite oberhalb von „Ressourcengruppen“ die Option **Alle Dienste** aus.

#### Aufgabe 3:  Bei dieser Aufgabe gehen Sie den Prozess zum Herstellen der Verbindung zwischen Azure Sentinel und Ihrer Datenquelle durch, um mit dem Sammeln von Daten zu beginnen. Hinweis: Es kann einige Zeit in Anspruch nehmen, bis der verbundene Status eines Connectors angezeigt wird (~ 30 Minuten, je nach Mandant).

1. Geben Sie auf der Seite „Alle Dienste“ den Text **Azure Sentinel** in das Feld „Dienste filtern“ ein. Wählen Sie dann **Azure Sentinel** aus der Liste mit den Ergebnissen aus. 

2. Wählen Sie auf der Seite „Azure Sentinel“ den von Ihnen mit der Azure Sentinel-Instanz erstellten Arbeitsbereich aus, nämlich **SC900-LogAnalytics-workspace**.

3. Der erste Schritt mit Azure Sentinel besteht darin, Daten sammeln zu können. Wählen Sie im linken Navigationsbereich die unter der Konfiguration aufgelistete Option **Datenconnectors** aus.

4. Scrollen Sie auf der Seite „Datenconnectors“ nach unten zum Hauptfenster, um die ausführliche Liste mit den verfügbaren Connectors anzuzeigen. Geben Sie in das Suchfeld der Seite „Datenconnectors“ den Text **Azure** ein. Wählen Sie dann in der Liste den Eintrag **Azure Active Directory** aus.

5. Das Fenster „Azure Active Directory Connector“ wird geöffnet.  Wählen Sie **Connectorseite öffnen** aus.

6. Überprüfen Sie auf der Azure Active Directory Connector-Seite die Beschreibung, und beachten Sie den zugehörigen Inhalt, der Arbeitsmappe, Abfragen und Regelvorlagen für Analysen umfasst.  

7. Die Registerkarte „Anweisungen“ im Hauptfenster umfasst die Voraussetzungen für die Integration von Azure Sentinel in Azure Active Directory.   Wählen Sie unter „Konfiguration“ die Option **Anmeldeprotokolle** und dann „Änderungen anwenden“ (es können mehrere Connectors ausgewählt werden) aus.

8. Beachten Sie auf der Registerkarte „Nächste Schritte“ die Liste mit den empfohlenen Arbeitsmappen.   Wählen Sie unter „Empfohlene Arbeitsmappen“ die Option **Azure-Anmeldeprotokolle** (es können zusätzliche Arbeitsmappen ausgewählt werden) aus.

9. Wählen Sie auf der Seite „Arbeitsmappen“ auf der ausgewählten (unterstrichenen) Registerkarte „Vorlagen“ die Option **Azure-Anmeldeprotokolle** aus. 

10. Überprüfen Sie im Fenster „Azure Active Directory-Anmeldeprotokolle“, das geöffnet wird, die Beschreibung, und wählen Sie **Vorlage anzeigen** aus.  Schließen Sie die Vorlage. Wählen Sie dazu in der oberen rechten Ecke des Bildschirms das **X** aus.  Wählen Sie unten auf der Seite **Speichern** aus. Wählen Sie dann **OK** aus, um die Arbeitsmappe am Standardspeicherort zu speichern.

11. Wählen Sie in der oberen linken Ecke der Seite „Arbeitsmappe“ oberhalb des Texts „Arbeitsmappen“ die Option **Azure Sentinel** aus. Dadurch gelangen Sie zur Seite „Datenconnectors“ von Azure Sentinel zurück.

12. Oben auf der Seite „Datenconnectors“ sollte „1 verbunden“ angezeigt werden, um anzugeben, dass Sie nun mit Azure Active Directory verbunden sind.

13. Wählen Sie im linken Navigationsbereich **Arbeitsmappen** aus.

14. Wählen Sie auf der Seite „Arbeitsmappen“ die Registerkarte **Meine Arbeitsmappen** aus, die sich oberhalb des Suchfelds befindet.  Die von Ihnen soeben gespeicherte Arbeitsmappe wird aufgelistet und steht Ihnen zum Anzeigen und Überwachen Ihrer Daten zur Verfügung.

15. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Aufgabe 4:  Bei dieser Aufgabe gehen Sie den Prozess der Verwendung einer integrierten Regelvorlage für Analysen durch, um eine Regel zu erstellen, damit Sie bei verdächtigen Aktivitäten benachrichtigt werden.

1. Wählen Sie im linken Navigationsbereich **Analysen** aus.

2. Auf der Seite „Analysen“ werden aktive Regeln („Erweiterte Erkennung von mehrstufigen Angriffen“ ist standardmäßig aktiviert) angezeigt. Außerdem bietet sie Zugriff auf „Regelvorlagen“.  Wählen Sie die Registerkarte **Regelvorlagen** aus.  Beachten Sie die Liste der verfügbaren Vorlagen und die unterschiedlichen Arten zum Filtern der Liste.  Mit den integrierten Analysewarnungen im Azure Sentinel-Arbeitsbereich werden sie sofort über verdächtige Aktivitäten informiert.

3. Geben Sie **Azure-Portal** in die Suchleiste ein.  Wählen Sie **Fehlgeschlagene Anmeldeversuche beim Azure-Portal** aus.  

4. Lesen Sie im Fenster, das geöffnet wird, die Beschreibung, und überprüfen Sie die der Vorlage zugeordneten Informationen.  Wählen Sie unten auf der Seite **Regel erstellen** aus.

5. Überprüfen Sie im Assistenten für Analyseregeln die Informationen, und wählen Sie **Weiter: Regellogik festlegen >** aus.

6. Auf der Seite „Regellogik festlegen“ definieren Sie die Logik für Ihre neue Analyseregel. Die Vorlage umfasst bereits eine gewisse Logik und vordefinierte Einstellungen.  Scrollen Sie durch die Seite, um die verfügbaren Einstellungen anzuzeigen.  Übernehmen Sie die Standardwerte. Wählen Sie **Weiter: Incidenteinstellungen (Vorschau) >** aus.

7. Mithilfe von „Incidenteinstellungen“ können Azure Sentinel-Warnungen gemeinsam in einen Incident gruppiert werden, der angezeigt werden sollte. Sie können festlegen, ob die durch diese Analyseregel ausgelösten Warnungen Incidents generieren sollen.  Übernehmen Sie die Standardeinstellungen, und wählen Sie **Weiter: Automatisierte Antwort >** aus.

8. Beachten Sie auf der Registerkarte „Automatisierte Antwort“, wie Sie ein Playbook zum Automatisieren der Antwort hinzufügen können.  Ebenso können Sie eine Incidentautomatisierungsregel erstellen.  Wählen Sie **+ Neu hinzufügen** unter der Option für die Incidentautomatisierung aus.  Es wird ein Fenster zum Erstellen einer neuen Automatisierungsregel geöffnet.  Die von Ihnen auf dieser Seite erstellten Automatisierungsregeln werden durch Ihre erstellte Analyseregel ausgelöst. Beachten Sie, dass Sie Bedingungen hinzufügen und Aktionen für die Regel festlegen können.   Wählen Sie **Abbrechen** aus, um das Fenster zu schließen.

9. Wählen Sie **Weiter: Überprüfen >** aus, um alle Details basierend auf der ausgewählten Vorlage zu überprüfen, die der Regel zugeordnet sind. An diesem Punkt können Sie die Regel erstellen, indem Sie **Erstellen** auswählen. Alternativ können Sie in der oberen rechten Ecke der Seite das **X** auswählen, um den Vorgang zu beenden, ohne die Regel zu erstellen.

10. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.

#### Aufgabe 5:  Bei der vorherigen Aufgabe haben Sie eine Analyseregel erstellt, um gewarnt zu werden, wenn verdächtige Aktivitäten auftreten.  Dieser Assistent enthält die Option, um die Antwort basierend auf der bestimmten Regel für einen Incident zu automatisieren.  Sie können Automatisierungsregeln aber auch direkt über die Option für die Automatisierungskonfiguration erstellen.

1. Wählen Sie im linken Navigationsbereich **Automation** aus.  

2. Wählen Sie **+ Erstellen** aus. Beachten Sie im Dropdown, dass Sie entweder ein neues Playbook oder eine neue Regel hinzufügen können.  Wählen Sie **Neue Regel hinzufügen** aus.  

3. Es wird ein Fenster zum Erstellen einer neuen Automatisierungsregel geöffnet.  Beachten Sie, dass Sie Bedingungen hinzufügen und Aktionen für die Regel festlegen können.  Der einzige Unterschied besteht darin, dass die erste Bedingung zum Zuordnen der Analyseregel(n) vorgesehen ist, auf die diese Automatisierungsregel angewendet werden soll(en).  Dies war in der vorherigen Aufgabe ausgegraut, da die Automatisierung für die bestimmte Regel konfiguriert wurde.  Wählen Sie **Abbrechen** aus, um das Fenster „Neue Automatisierungsregel erstellen“ zu schließen.

4. Lassen Sie diese Seite geöffnet, da Sie sie in der nächsten Aufgabe verwenden werden.


#### Aufgabe 6:  Löschen Sie die Azure Sentinel-Ressourcengruppe.  Azure Sentinel wird auf Grundlage der Datenmenge abgerechnet, die zur Analyse in Azure Sentinel erfasst wurde. Obwohl die im Rahmen dieses Labs erfasste Datenmenge gering ist, sollten Sie die Azure Sentinel-Ressourcengruppe löschen, nachdem Sie die Funktionen von Azure Sentinel erkundet haben.

1. Wählen Sie auf der Seite „Azure Sentinel“ in der oberen linken Ecke der Seite oberhalb des Texts „Azure Sentinel“ die Option **Alle Dienste** aus.

2. Geben Sie die Ressourcengruppen in das Feld „Dienste filtern“ ein. Wählen Sie dann in der bereitgestellten Liste den Eintrag **Ressourcengruppen** aus.

3. Wählen Sie auf der Seite „Ressourcengruppen“ die von Ihnen mit Azure Sentinel erstellte Ressourcengruppe aus, nämlich **SC900-ResourceGroup**.

4. Wählen Sie im oberen mittleren Bereich der Seite die Option **Ressourcengruppe löschen** aus.  Überprüfen Sie die Warnung.  Geben Sie den Namen der Ressourcengruppe **SC900-ResourceGroup** ein. Wählen Sie dann unten auf der Seite **Löschen** aus.  Es kann mehrere Minuten dauern, bis die Ressourcengruppe gelöscht ist.

5. Nachdem Sie die Löschung der Ressourcengruppe überprüft haben, schließen Sie die Browserseite. 


#### Überprüfung

In diesem Lab sind Sie den Prozess der Erstellung einer Azure Sentinel-Instanz durchgegangen.  Sie haben zudem die Berechtigungen eingerichtet, um den Zugriff auf die der Azure Sentinel-Instanz zugeordneten Ressourcen sicherzustellen.  Nach der Erstellung Ihrer Azure Sentinel-Instanz sind Sie die Schritte zum Herstellen der Verbindung zwischen Sentinel und Ihren Datenquellen durchgegangen. Außerdem haben Sie erfahren, wie integrierte Analyseregeln verwendet werden, um über verdächtige Aktivitäten benachrichtigt zu werden. Als Letztes haben Sie die Automatisierungsfunktion erkundet. Abgeschlossen haben Sie das Lab, indem Sie die Ressourcengruppe gelöscht haben, die der von Ihnen erstellten Azure Sentinel-Instanz zugeordnet ist.