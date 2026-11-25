# Datenschutzerklärung – Essensbestellung

**Letzte Aktualisierung:** 25. November 2026  
**Entwickler:** Martin Zanker  
**Kontakt:** martinzankerdevelopment@gmail.com

---

## 1. Allgemeines

Die App **Essensbestellung** ist eine interne iOS-Anwendung des Grundschulhorts Westend-Drachen (Elterninitiative e.V., München). Sie ist nur für das Team des Horts bestimmt und nur mit einem Konto des Horts nutzbar. Die App wird über den App Store als nicht öffentlich auffindbare App („Unlisted App“) sowie über Apple TestFlight verteilt.

Die App dient der Planung, Verwaltung und dem Versand der wöchentlichen Essensbestellung beim Caterer.

---

## 2. Erhobene Daten und Verwendungszweck

### 2.1 Anmeldung

Die App kann nur mit einem Konto des Horts genutzt werden. Konten legt ausschließlich der Hort an; eine Selbstregistrierung gibt es nicht. Verarbeitet werden:

- E-Mail-Adresse des Kontos
- Passwort (von Firebase Authentication nur verschlüsselt gespeichert)
- technische Nutzerkennung (Firebase-UID)

Die Anmeldung bleibt bis zur Abmeldung in der App im iOS-Schlüsselbund des Geräts gespeichert.

**Zweck:** Nur berechtigte Personen des Hort-Teams erhalten Zugriff auf die Bestelldaten.

### 2.2 Bestelldaten (lokal & Cloud)

Die App speichert lokal auf dem Gerät (SwiftData) und synchronisiert über Google Firebase Firestore:

- Kalenderwoche und Jahr der Bestellung
- Portionsanzahl (gesamt und vegetarisch) je Wochentag
- Auswahl von Speisen (Suppe, Hauptgericht, Nachspeise)
- Ferien-, Brotzeit- und Sondertage, Anmerkungen
- Sendestatus und Sendedatum
- Bewertungen der Gerichte (Menge, Zubereitung, Beliebtheit)

Die App verarbeitet **keine Namen oder sonstigen Daten von Kindern oder Eltern**.

**Zweck:** Verwaltung der wöchentlichen Essensbestellung; alle Geräte des Teams sehen denselben Stand.

### 2.3 Speisenliste (lokal & Cloud)

- Name und Typ der Speise (Suppe, Gericht, Nachspeise)
- Sortierindex und Verwendungsverlauf

**Zweck:** Wiederverwendung häufig bestellter Gerichte.

### 2.4 E-Mail-Einstellungen

- Mailserver, Port und Benutzername (lokal und Cloud)
- Absender-, Empfänger- (Caterer) und BCC-Adressen mit Namen (lokal und Cloud)
- Passwort des Mailkontos: ausschließlich verschlüsselt im iOS-Schlüsselbund des jeweiligen Geräts, **nicht** in der Cloud

**Zweck:** Versand der Bestellung per E-Mail an den Caterer.

### 2.5 PDF-Erzeugung

Aus den Bestelldaten wird ein PDF lokal auf dem Gerät erzeugt – für den Mailversand, die Vorschau und zum Teilen, wenn das Team dies auslöst.

### 2.6 Technische Prüfung (App Check)

Über Firebase App Check und Apple App Attest wird geprüft, dass Anfragen an die Datenbank von der echten App stammen. Dabei werden keine Inhalte und keine personenbezogenen Daten des Teams übertragen.

---

## 3. Verwendete Dienste Dritter

### Google Firebase (Firestore, Authentication, App Check)

Anbieter ist Google Ireland Limited, Gordon House, Barrow Street, Dublin 4, Irland. Firestore speichert die Daten in der Europäischen Union. Google verarbeitet die Daten im Auftrag; eine Übermittlung in die USA ist dabei nicht ausgeschlossen und erfolgt auf Grundlage des EU-US Data Privacy Framework bzw. von Standardvertragsklauseln.

- Datenschutzhinweise von Firebase: https://firebase.google.com/support/privacy

### Mailserver des Horts

Die Bestellung wird über den in den Einstellungen hinterlegten Mailserver an den Caterer gesendet; eine Kopie wird im Ordner „Gesendet“ dieses Mailkontos abgelegt.

---

## 4. Nicht erhobene Daten

Die App erhebt **keine** der folgenden Daten:

- Kamera oder Fotos
- Standortdaten
- Kontakte
- Kalender
- Biometrische Daten
- Daten von Kindern oder Eltern
- Nutzungs- oder Analysedaten (keine Werbung, kein Tracking)

---

## 5. Datenweitergabe an Dritte

Daten werden nur an die oben genannten Dienste und – mit der Bestellung – an den Caterer weitergegeben. Es findet keine Weitergabe zu Werbe- oder Analysezwecken statt.

---

## 6. Datensicherheit

- Zugriff auf die Datenbank nur für angemeldete Konten des Horts, die vom Hort freigeschaltet wurden.
- Anfragen werden zusätzlich per App Check geprüft.
- Passwörter von Mailkonten werden verschlüsselt im iOS-Schlüsselbund gespeichert.
- Die Kommunikation mit Firebase und dem Mailserver erfolgt verschlüsselt (TLS bzw. STARTTLS).

---

## 7. Speicherdauer

Bestellungen und Speisen bleiben gespeichert, solange sie für die Organisation des Horts benötigt werden. Konten von Personen, die das Team verlassen, werden gelöscht. Auf Anfrage werden Daten gelöscht, soweit keine Aufbewahrungspflichten entgegenstehen.

---

## 8. Rechte der Betroffenen

Sie haben das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Datenübertragbarkeit und Widerspruch. Außerdem können Sie sich bei einer Datenschutz-Aufsichtsbehörde beschweren, in Bayern beim Bayerischen Landesamt für Datenschutzaufsicht (BayLDA).

---

## 9. Kontakt

Bei Fragen zum Datenschutz wenden Sie sich bitte an:

**Martin Zanker**  
E-Mail: martinzankerdevelopment@gmail.com
