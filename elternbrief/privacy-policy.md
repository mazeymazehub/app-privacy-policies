# Datenschutzerklärung – Elternbrief

**Letzte Aktualisierung:** 25. November 2026  
**Entwickler:** Martin Zanker  
**Kontakt:** martinzankerdevelopment@gmail.com

---

## 1. Allgemeines

Die App **Elternbrief** ist eine interne iOS- und iPadOS-Anwendung des Grundschulhorts Westend-Drachen (Elterninitiative e.V., München). Sie ist nur für das Team des Horts bestimmt und nur mit einem Konto des Horts nutzbar. Die App wird über den App Store als nicht öffentlich auffindbare App („Unlisted App“) sowie über Apple TestFlight verteilt.

Die App dient der Erstellung des wöchentlichen Wochenplans und dem Versand des Elternbriefs.

---

## 2. Erhobene Daten und Verwendungszweck

### 2.1 Anmeldung

Die App kann nur mit einem Konto des Horts genutzt werden. Konten legt ausschließlich der Hort an; eine Selbstregistrierung gibt es nicht. Verarbeitet werden:

- E-Mail-Adresse des Kontos
- Passwort (von Firebase Authentication nur verschlüsselt gespeichert)
- technische Nutzerkennung (Firebase-UID)

Die Anmeldung bleibt bis zur Abmeldung in der App im iOS-Schlüsselbund des Geräts gespeichert.

**Zweck:** Nur berechtigte Personen des Hort-Teams erhalten Zugriff auf die Daten.

### 2.2 Wochenplan-Daten (lokal & Cloud)

Die App speichert lokal (SwiftData) und synchronisiert über Google Firebase Firestore:

- Kalenderwoche und Jahr
- Aktivitäten und Ereignisse je Wochentag (Typ, Uhrzeit, Bezeichnung, Ort)
- Sonderveranstaltungen (z. B. Feiertage, Elternabend, geschlossener Hort)
- Abwesenheiten, Praktika und Seminare von Teammitgliedern mit deren Namen bzw. Vornamen
- bei Geburtstagsfeiern die **Vornamen der Geburtstagskinder**, sofern das Team sie einträgt
- Notizen sowie Betreff und Texte des Elternbriefs, Sendestatus und Sendedatum

**Zweck:** Erstellung des wöchentlichen Wochenplans und des Elternbriefs.

### 2.3 Textbausteine und Teamliste (lokal & Cloud)

- wiederverwendbare Textbausteine
- Namen der Teammitglieder (für Abwesenheiten und Vertretungen)

**Zweck:** Vereinfachte Brieferstellung; einheitliche Daten auf allen Geräten des Teams.

### 2.4 Ortssuche (Apple MapKit)

Bei der Eingabe von Veranstaltungsorten wird die Apple-Ortssuche verwendet. Dabei werden nur die eingegebenen Suchbegriffe an Apple übermittelt; GPS-Standortdaten des Geräts werden **nicht** verwendet.

### 2.5 E-Mail-Versand

- Mailserver, Port und Benutzername (lokal und Cloud)
- Absender-, Empfänger- und BCC-Adressen mit Namen (lokal und Cloud)
- Passwort des Mailkontos: ausschließlich verschlüsselt im iOS-Schlüsselbund des jeweiligen Geräts, **nicht** in der Cloud

Der Elternbrief wird mit dem Wochenplan als PDF über den Mailserver des Horts versendet; eine Kopie wird im Ordner „Gesendet“ dieses Mailkontos abgelegt.

### 2.6 PDF-Erzeugung und Logo

Der Wochenplan wird lokal als PDF erzeugt. Ein Logo für den Wochenplan kann aus Fotos oder Dateien gewählt werden; die App erhält dabei nur das ausgewählte Bild.

### 2.7 Technische Prüfung (App Check)

Über Firebase App Check und Apple App Attest wird geprüft, dass Anfragen an die Datenbank von der echten App stammen. Dabei werden keine personenbezogenen Daten übertragen.

---

## 3. Verwendete Dienste Dritter

### Google Firebase (Firestore, Authentication, App Check)

Anbieter ist Google Ireland Limited, Gordon House, Barrow Street, Dublin 4, Irland. Firestore speichert die Daten in der Europäischen Union. Google verarbeitet die Daten im Auftrag; eine Übermittlung in die USA ist dabei nicht ausgeschlossen und erfolgt auf Grundlage des EU-US Data Privacy Framework bzw. von Standardvertragsklauseln.

- Datenschutzhinweise von Firebase: https://firebase.google.com/support/privacy

### Apple (MapKit, App Attest)

- Datenschutzrichtlinie von Apple: https://www.apple.com/de/legal/privacy/

Die App nutzt **keine** Analyse-, Werbe- oder Tracking-Dienste.

---

## 4. Nicht erhobene Daten

- Kamera, Mikrofon
- GPS-Standortdaten
- Kontakte, Kalender
- Biometrische Daten
- Nachnamen, Adressen oder Kontaktdaten von Kindern und Eltern
- Nutzungs- oder Analysedaten

---

## 5. Datenweitergabe an Dritte

Daten werden nur an die oben genannten Dienste und – mit dem Elternbrief – an die Empfängeradressen des Horts weitergegeben. Es findet keine Weitergabe zu Werbe- oder Analysezwecken statt.

---

## 6. Datensicherheit

- Zugriff auf die Datenbank nur für angemeldete, vom Hort freigeschaltete Konten; zusätzlich App Check.
- Passwörter von Mailkonten liegen verschlüsselt im iOS-Schlüsselbund.
- Die Kommunikation mit Firebase und dem Mailserver erfolgt verschlüsselt (TLS bzw. STARTTLS).

---

## 7. Speicherdauer

Wochenpläne und Briefe bleiben gespeichert, solange sie für die Organisation des Horts benötigt werden. Konten von Personen, die das Team verlassen, werden gelöscht. Auf Anfrage werden Daten gelöscht, soweit keine Aufbewahrungspflichten entgegenstehen.

---

## 8. Rechte der Betroffenen

Sie haben das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Datenübertragbarkeit und Widerspruch. Außerdem können Sie sich bei einer Datenschutz-Aufsichtsbehörde beschweren, in Bayern beim Bayerischen Landesamt für Datenschutzaufsicht (BayLDA).

---

## 9. Kontakt

Bei Fragen zum Datenschutz wenden Sie sich bitte an:

**Martin Zanker**  
E-Mail: martinzankerdevelopment@gmail.com
