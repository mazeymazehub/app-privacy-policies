# Datenschutzerklärung – DrachenScanner

**Letzte Aktualisierung:** 25. November 2026  
**Entwickler:** Martin Zanker  
**Kontakt:** martinzankerdevelopment@gmail.com

---

## 1. Allgemeines

Die App **DrachenScanner** ist eine interne iOS- und iPadOS-Anwendung des Grundschulhorts Westend-Drachen (Elterninitiative e.V., München). Sie ist nur für das Team des Horts bestimmt und nur mit einem Konto des Horts nutzbar. Die App wird über den App Store als nicht öffentlich auffindbare App („Unlisted App“) sowie über Apple TestFlight verteilt.

Die App dient der Erfassung von Kassenbelegen und der Erstellung der monatlichen Abrechnung.

---

## 2. Erhobene Daten und Verwendungszweck

### 2.1 Anmeldung

Die App kann nur mit einem Konto des Horts genutzt werden. Konten legt ausschließlich der Hort an; eine Selbstregistrierung gibt es nicht. Verarbeitet werden:

- E-Mail-Adresse des Kontos
- Passwort (von Firebase Authentication nur verschlüsselt gespeichert)
- technische Nutzerkennung (Firebase-UID)

**Zweck:** Nur berechtigte Personen des Hort-Teams erhalten Zugriff auf die Belege.

### 2.2 Kamera, Fotos und Texterkennung

Die App benötigt Zugriff auf die **Kamera** bzw. die **Fotomediathek**, um Belege zu fotografieren oder vorhandene Fotos und PDF-Rechnungen zu importieren. Die Texterkennung (Datum, Betrag, Geschäft) erfolgt **ausschließlich auf dem Gerät** (Apple Vision).

### 2.3 Belegdaten (lokal & Cloud)

Die App speichert lokal und synchronisiert über Google Firebase:

- je Beleg: Belegnummer, Datum, Geschäft, Kategorie, Betrag und Prüfstatus (Firestore)
- das Belegfoto bzw. die PDF-Rechnung (Firebase Storage)
- Monatsabrechnungen mit ihren Listen

**Zweck:** Monatliche Abrechnung der Ausgaben des Horts auf allen Geräten des Teams.

### 2.4 Unterschriften und Angaben zum Hort

- Name und Bild der Unterschrift der Personen, die Abrechnungen unterschreiben (lokal und Cloud)
- Name, Anschrift und Logo des Horts für die Abrechnung

**Zweck:** Erstellung der unterschriebenen Abrechnung als PDF bzw. Excel-Datei.

### 2.5 Versand und Archiv

- Abrechnungen können per E-Mail über den Mailserver des Horts versendet werden. Das Passwort des Mailkontos liegt ausschließlich verschlüsselt im iOS-Schlüsselbund des Geräts.
- Abrechnungen können in einem vom Team gewählten Ordner (z. B. in iCloud Drive) archiviert werden.
- Exportierte PDF- und Excel-Dateien verlassen das Gerät nur, wenn das Team sie aktiv versendet, teilt oder archiviert.

### 2.6 Technische Prüfung (App Check)

Über Firebase App Check und Apple App Attest wird geprüft, dass Anfragen von der echten App stammen. Dabei werden keine personenbezogenen Daten übertragen.

---

## 3. Verwendete Dienste Dritter

### Google Firebase (Firestore, Storage, Authentication, App Check)

Anbieter ist Google Ireland Limited, Gordon House, Barrow Street, Dublin 4, Irland. Firestore speichert die Daten in der Europäischen Union. Google verarbeitet die Daten im Auftrag; eine Übermittlung in die USA ist dabei nicht ausgeschlossen und erfolgt auf Grundlage des EU-US Data Privacy Framework bzw. von Standardvertragsklauseln.

- Datenschutzhinweise von Firebase: https://firebase.google.com/support/privacy

Die App nutzt **keine** Analyse-, Werbe- oder Tracking-Dienste.

---

## 4. Nicht erhobene Daten

- Standortdaten
- Kontakte, Kalender
- Biometrische Daten
- Daten von Kindern oder Eltern
- Nutzungs- oder Analysedaten

---

## 5. Berechtigungen

| Berechtigung   | Zweck                                   |
|----------------|-----------------------------------------|
| Kamera         | Belege fotografieren                    |
| Fotomediathek  | Vorhandene Belegfotos importieren       |

Erteilte Berechtigungen können jederzeit in den iOS-Einstellungen widerrufen werden.

---

## 6. Datenweitergabe an Dritte

Daten werden nur an die oben genannten Dienste und – beim Versand einer Abrechnung – an die vom Team gewählten Empfänger weitergegeben. Es findet keine Weitergabe zu Werbe- oder Analysezwecken statt.

---

## 7. Datensicherheit

- Zugriff auf Datenbank und Belegfotos nur für angemeldete, vom Hort freigeschaltete Konten; zusätzlich App Check.
- Die Kommunikation mit Firebase und dem Mailserver erfolgt verschlüsselt (TLS bzw. STARTTLS).

---

## 8. Speicherdauer

Belege und Abrechnungen bleiben gespeichert, solange sie für die Abrechnung und gesetzliche Aufbewahrungspflichten benötigt werden. Konten von Personen, die das Team verlassen, werden gelöscht.

---

## 9. Rechte der Betroffenen

Sie haben das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Datenübertragbarkeit und Widerspruch, soweit keine Aufbewahrungspflichten entgegenstehen. Außerdem können Sie sich bei einer Datenschutz-Aufsichtsbehörde beschweren, in Bayern beim Bayerischen Landesamt für Datenschutzaufsicht (BayLDA).

---

## 10. Kontakt

Bei Fragen zum Datenschutz wenden Sie sich bitte an:

**Martin Zanker**  
E-Mail: martinzankerdevelopment@gmail.com
