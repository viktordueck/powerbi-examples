# Row Level Security (RLS) in Power BI

- Artikel mit Video: https://www.viktordueck.de/row-level-security-in-powerbi
- PBIX Datei: https://github.com/viktordueck/powerbi-examples/raw/main/Row%20Level%20Security/RLS.pbix

- Deutsch: Sicherheit auf Zeilenebene

* Beschränkt die Sicht auf Daten für bestimmte Anwender oder Anwendergruppen

* "Eingeschränkte" Sicht auf Daten gilt dann im Power BI Service und bei Analysen in Excel, jedoch nicht wenn die Datei in Power BI Desktop geöffnet wird

* Zu beachten ist welche Rechte die Anwender im Arbeitsbereich haben, RSL greift nur bei dem Recht "Anzeige". Sobald Anwender Mitwirkende oder höher sind, greift RLS nicht mehr.

## Umsetzung

- RLS-Gruppen und Rechte werden in Power BI Desktop definiert
- Die Benutzer müssen dann im Service den RLS-Gruppen hinzugefügt werden

## Statisches vs. dynamisches RLS

- Bei statischem RLS wird jeder Benutzer einer RLS-Gruppe hinzugefügt und diese RLS-Gruppe definiert welche Daten sichtbar sind
- Bei dynamischen RLS (DRLS) wird die Email-Adresse des eingeloggten Benutzers verwendet, um zu definieren welche Daten im Modell der Benutzer sehen darf.

## RLS vs. Object Level Security (OLS)

- Bei OLS werden ganze Tabellen für Anwender(gruppen) ausgeblendet, als würden sie im Modell gar nicht existieren.
- OLS kann aktuell nicht in Power BI Desktop konfiguriert werden, jedoch mit Tabular Edit
