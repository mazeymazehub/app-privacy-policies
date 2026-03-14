# Datenschutzerklärung – Essensbestellung

**Letzte Aktualisierung:** März 2025  
**Entwickler:** Martin Zanker  
**Kontakt:** martinzankerdevelopment@gmail.com

---

## 1. Allgemeines

Die App **Essensbestellung** ist eine interne iOS-Anwendung für den Grundschulhort und wird ausschließlich über Apple TestFlight verteilt. Sie ist nicht im App Store veröffentlicht. Die App dient der Erfassung, Verwaltung und dem Versand von Essensbestellungen für den Hortbetrieb.

Diese Datenschutzerklärung informiert darüber, welche Daten die App erhebt, wie sie verarbeitet werden und zu welchem Zweck.

---

## 2. Erhobene Daten und Verwendungszweck

### 2.1 Bestelldaten (lokal & Cloud)

Die App speichert folgende Bestelldaten lokal auf dem Gerät (via SwiftData) und synchronisiert sie über Google Firebase Firestore:

- Kalenderwoche und Jahr der Bestellung
- Portionsanzahl (gesamt und vegetarisch) je Wochentag
- Auswahl von Speisen (Suppe, Hauptgericht, Nachspeise)
- Sonderveranstaltungen und -ereignisse
- Sendestatus und Sendedatum
- Bewertungen der Gerichte

**Zweck:** Verwaltung der wöchentlichen Essensbestellung und Synchronisation zwischen mehreren Geräten innerhalb des Hortteams.

### 2.2 Speisenliste (lokal & Cloud)

Die App speichert eine Speisenliste (Suppen, Gerichte, Nachspeisen) lokal und in der Cloud:

- Name der Speise
- Typ (Suppe, Gericht, Nachspeise)
- Sortierindex und Verwendungsverlauf

**Zweck:** Wiederverwendung häufig bestellter Gerichte zur vereinfachten Bestelleingabe.

### 2.3 E-Mail- und SMTP-Einstellungen

Für den Versand der Bestellungen per E-Mail werden folgende Einstellungen gespeichert:

- SMTP-Server, Port und Benutzername (lokal in UserDefaults und Cloud)
- SMTP-Passwort (verschlüsselt im iOS Keychain gespeichert, **nicht** in der Cloud)
- Absender- und Empfängeradressen (Name und E-Mail)
- BCC-Adresse

**Zweck:** Automatischer E-Mail-Versand der Essensbestellung als PDF-Anhang an den Essensanbieter.

### 2.4 Firebase Authentication

Die App nutzt **Firebase Anonymous Authentication**. Dabei wird eine anonyme Benutzer-ID erstellt, ohne dass persönliche Informationen wie Name oder E-Mail-Adresse erfasst werden.

**Zweck:** Zugriffskontrolle auf die Firestore-Datenbank.

### 2.5 PDF-Generierung

Aus den erfassten Bestelldaten wird ein PDF-Dokument erstellt und lokal gerendert.

**Zweck:** Versand der Bestellung per E-Mail und Vorschau in der App.

### 2.6 Geräteinterne Einstellungen

Folgende Einstellungen werden lokal auf dem Gerät gespeichert (UserDefaults):

- Standardwerte für Portionsanzahl und vegetarische Portionen
- Konfiguration des Brotzeittages

**Zweck:** Vereinfachung der wöchentlichen Dateneingabe durch Vorbelegen von Standardwerten.

---

## 3. Verwendete Dienste Dritter

### Google Firebase (Firestore & Authentication)

Die App nutzt Google Firebase, einen Cloud-Dienst von Google LLC, für die Datensynchronisation und anonyme Authentifizierung. Die Daten werden auf Servern von Google gespeichert.

- Datenschutzerklärung von Google/Firebase: https://firebase.google.com/support/privacy

Die in der Cloud gespeicherten Daten enthalten **keine personenbezogenen Daten** der Kinder oder Eltern – ausschließlich operative Bestelldaten des Hortteams.

---

## 4. Nicht erhobene Daten

Die App erhebt **keine** der folgenden Daten:

- Kamera oder Fotos
- Standortdaten
- Kontakte
- Kalender
- Biometrische Daten
- Daten von Kindern oder Eltern

---

## 5. Datenweitergabe an Dritte

Es werden **keine personenbezogenen Daten an Dritte weitergegeben**. Die SMTP-Zugangsdaten werden ausschließlich lokal im iOS Keychain gespeichert und niemals übertragen. Die Cloud-Synchronisation über Firebase dient ausschließlich der internen Nutzung durch das Hortteam.

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
