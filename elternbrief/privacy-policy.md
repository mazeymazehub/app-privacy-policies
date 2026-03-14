# Datenschutzerklärung – Elternbrief

**Letzte Aktualisierung:** März 2025  
**Entwickler:** Martin Zanker  
**Kontakt:** martinzankerdevelopment@gmail.com

---

## 1. Allgemeines

Die App **Elternbrief** ist eine interne iOS-Anwendung für den Grundschulhort und wird ausschließlich über Apple TestFlight verteilt. Sie ist nicht im App Store veröffentlicht. Die App dient der Erstellung und dem Versand des wöchentlichen Elternbriefs sowie des zugehörigen Wochenplans.

Diese Datenschutzerklärung informiert darüber, welche Daten die App erhebt, wie sie verarbeitet werden und zu welchem Zweck.

---

## 2. Erhobene Daten und Verwendungszweck

### 2.1 Wochenplan-Daten (lokal & Cloud)

Die App speichert folgende Wochenplan-Daten lokal auf dem Gerät (via SwiftData) und synchronisiert sie über Google Firebase Firestore:

- Kalenderwoche und Jahr
- Aktivitäten und Ereignisse je Wochentag (Typ, Uhrzeit, Bezeichnung)
- Veranstaltungsorte (Name und Apple-Maps-Link)
- Sonderveranstaltungen (z. B. Feiertage, Elternabend, geschlossener Hort)
- Notizen und Betreffzeile des Elternbriefs
- Sendestatus und Sendedatum

**Zweck:** Erstellung des wöchentlichen Wochenplans und automatische Generierung des Elternbriefs.

### 2.2 Elternbrief-Daten (lokal & Cloud)

Die App erstellt automatisch oder manuell einen Elternbrief mit folgenden Inhalten:

- Anrede, Einleitung, variable Textabschnitte, Grußformel
- Betreffzeile
- Sendestatus und -datum

**Zweck:** Vorbereitung und Versand des wöchentlichen Elternbriefs per E-Mail.

### 2.3 Textbausteine (lokal & Cloud)

Wiederverwendbare Textabschnitte (Textbausteine) werden lokal und in der Cloud gespeichert:

- Bezeichnung und Inhalt des Textbausteins
- Erstellungs- und Änderungsdatum

**Zweck:** Vereinfachung der Brieferstellung durch vordefinierte, wiederverwendbare Texte.

### 2.4 Teamdaten

Namen der Teammitglieder (Erzieherpersonal) werden lokal auf dem Gerät gespeichert (UserDefaults).

**Zweck:** Anzeige von Abwesenheiten einzelner Teammitglieder im Wochenplan und Elternbrief.

### 2.5 Ortssuche (Apple MapKit)

Bei der Eingabe von Veranstaltungsorten wird die **Apple MapKit-Ortssuche** verwendet. Die eingegebenen Suchbegriffe werden an Apple übermittelt, um Vorschläge für Orte oder Points of Interest zurückzugeben.

- Es werden nur Suchanfragen (Texteingaben) übermittelt.
- Es werden **keine GPS-Standortdaten** des Geräts verwendet oder übertragen.

**Zweck:** Komfortable Suche und Auswahl von Veranstaltungsorten für den Wochenplan.

- Datenschutzerklärung von Apple Maps: https://www.apple.com/de/privacy/

### 2.6 E-Mail- und SMTP-Einstellungen

Für den Versand des Elternbriefs per E-Mail werden folgende Einstellungen gespeichert:

- SMTP-Server, Port und Benutzername (lokal in UserDefaults und Cloud)
- SMTP-Passwort (verschlüsselt im iOS Keychain gespeichert, **nicht** in der Cloud)
- Absender- und Empfängeradressen (Name und E-Mail)
- BCC-Adresse

**Zweck:** Automatischer E-Mail-Versand des Elternbriefs mit angehängtem Wochenplan als PDF.

### 2.7 Firebase Authentication

Die App nutzt **Firebase Anonymous Authentication**. Dabei wird eine anonyme Benutzer-ID erstellt, ohne dass persönliche Informationen wie Name oder E-Mail-Adresse erfasst werden.

**Zweck:** Zugriffskontrolle auf die Firestore-Datenbank.

### 2.8 PDF-Generierung

Aus den Wochenplan-Daten wird ein PDF-Dokument erstellt und lokal gerendert.

**Zweck:** Versand als Anhang im Elternbrief und Vorschau in der App.

### 2.9 Geräteinterne Einstellungen

Folgende Einstellungen werden lokal auf dem Gerät gespeichert (UserDefaults):

- SMTP-Konfiguration
- Synchronisierungs-Zeitstempel

**Zweck:** Persistenz der App-Konfiguration über Sitzungen hinweg.

---

## 3. Verwendete Dienste Dritter

### Google Firebase (Firestore & Authentication)

Die App nutzt Google Firebase, einen Cloud-Dienst von Google LLC, für die Datensynchronisation und anonyme Authentifizierung. Die Daten werden auf Servern von Google gespeichert.

- Datenschutzerklärung von Google/Firebase: https://firebase.google.com/support/privacy

Die in der Cloud gespeicherten Daten enthalten **keine personenbezogenen Daten** der Kinder oder Eltern – ausschließlich operative Planungsdaten des Hortteams.

### Apple MapKit

Bei der Standortsuche für Veranstaltungsorte werden Texteingaben an den Apple-Suchdienst übermittelt. Es werden keine GPS-Daten verwendet.

- Datenschutzerklärung von Apple: https://www.apple.com/de/privacy/

---

## 4. Nicht erhobene Daten

Die App erhebt **keine** der folgenden Daten:

- Kamera oder Fotos
- GPS-Standortdaten
- Kontakte
- Kalender
- Biometrische Daten
- Personenbezogene Daten der Kinder oder Eltern

---

## 5. Datenweitergabe an Dritte

Es werden **keine personenbezogenen Daten an Dritte weitergegeben**. Die SMTP-Zugangsdaten werden ausschließlich lokal im iOS Keychain gespeichert und niemals an Dritte übermittelt. Die Cloud-Synchronisation über Firebase und die Ortssuche über Apple MapKit dienen ausschließlich der internen Nutzung durch das Hortteam.

---

## 6. Datensicherheit

- SMTP-Passwörter werden verschlüsselt im iOS Keychain gespeichert.
- Die Kommunikation mit dem SMTP-Server erfolgt verschlüsselt via TLS oder STARTTLS.
- Der Zugriff auf Firebase Firestore ist durch anonyme Authentifizierung abgesichert.

---

## 7. Verbreitung und Nutzerkreis

Die App wird ausschließlich über **Apple TestFlight** an das Hortteam verteilt und ist nicht öffentlich zugänglich. Sie ist nicht im App Store erhältlich.

---

## 8. Kontakt

Bei Fragen zum Datenschutz wenden Sie sich bitte an:

**Martin Zanker**  
E-Mail: martinzankerdevelopment@gmail.com
