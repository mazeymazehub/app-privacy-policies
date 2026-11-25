# Datenschutzerklärung – Brotzeit

**Letzte Aktualisierung:** 25. November 2026  
**Entwickler:** Martin Zanker  
**Kontakt:** martinzankerdevelopment@gmail.com

---

## 1. Allgemeines

Die App **Brotzeit** ist eine interne iOS- und iPadOS-Anwendung für den Grundschulhort Westend-Drachen (Elterninitiative e. V., München). Sie ist nur mit einem Konto des Horts nutzbar und wird über den App Store als nicht öffentlich auffindbare App („Unlisted App“) sowie über Apple TestFlight verteilt.

Die App ersetzt die bisherige Papierliste für den Brotzeittag: Die Kinder tragen auf den Hort-iPads ein, ob sie am Brotzeittag im Hort sind und was sie essen möchten. Das Hortteam legt die Brotzeiten an, behält den Überblick über fehlende Einträge und erstellt daraus eine Einkaufsliste als PDF.

Diese Datenschutzerklärung informiert darüber, welche Daten die App erhebt, wie sie verarbeitet werden und zu welchem Zweck.

---

## 2. Erhobene Daten und Verwendungszweck

### 2.1 Namensliste (lokal & Cloud)

Die App speichert eine Liste der Kinder und Teammitglieder lokal auf dem Gerät (SwiftData) und synchronisiert sie über Google Firebase Firestore:

- **Vorname** (kein Nachname, kein Geburtsdatum, keine Kontaktdaten)
- Kennzeichnung, ob es sich um ein Kind oder ein Teammitglied handelt
- Kennzeichnung »1. Klasse« – diese Kinder wählen über große Bilder statt über Text aus, da sie meist noch nicht lesen können
- Position in der Liste (Reihenfolge)

**Zweck:** Anzeige der Namen in der Abfrage und Zuordnung der Einträge.

### 2.2 Brotzeiten und Einträge (lokal & Cloud)

- Datum der Brotzeit und Art (warm oder kalt)
- je Person: ob sie am Brotzeittag im Hort ist, welche Lebensmittel sie möchte und in welcher Menge

**Zweck:** Planung des Einkaufs, Übersicht über fehlende Einträge und Erstellung der Brotzeitliste als PDF.

Es werden **keine** Angaben zu Allergien, Unverträglichkeiten oder sonstigen Gesundheitsdaten erhoben.

### 2.3 Einstellungen (lokal & Cloud)

- Auswahl der Lebensmittel und Kategorien
- Wochentag der Brotzeit
- Team-PIN, die den Team-Bereich auf den Hort-iPads vor den Kindern schützt
- Anzeigeoption für die 1. Klasse (Groß- oder Kleinbuchstaben)

**Zweck:** Einheitliche Konfiguration auf allen Geräten des Hortes.

### 2.4 Anmeldung (Firebase Authentication)

Die App kann nur mit einem Konto des Horts genutzt werden; die Hort-iPads sind mit einem gemeinsamen Hort-Konto angemeldet. Konten legt ausschließlich der Hort an; eine Selbstregistrierung gibt es nicht. Verarbeitet werden die E-Mail-Adresse des Kontos, das Passwort (von Firebase nur verschlüsselt gespeichert) und eine technische Nutzerkennung. Die Kinder melden sich nicht an und haben keine eigenen Konten.

**Zweck:** Zugriffskontrolle auf die Firestore-Datenbank.

### 2.5 Firebase App Check

Die App nutzt **Firebase App Check** zusammen mit **Apple App Attest**. Dabei bestätigt das Gerät gegenüber Firebase, dass Anfragen von der echten, unveränderten App stammen. Es werden dabei keine personenbezogenen Daten der Nutzer übermittelt.

**Zweck:** Schutz der Datenbank vor unberechtigtem Zugriff.

### 2.6 Mitteilungen (nur iPhone)

Auf den iPhones des Teams erinnert die App am Vortag einer Brotzeit um 13:15 Uhr an fehlende Einträge (Vornamen der betroffenen Kinder bzw. deren Anzahl). Die Mitteilung wird **lokal auf dem Gerät** geplant; es wird kein Push-Server verwendet. Damit die Angaben aktuell sind, gleicht die App ihre Daten bei Bedarf im Hintergrund ab.

Die Berechtigung für Mitteilungen wird von der App abgefragt und kann jederzeit in den iOS-Einstellungen widerrufen werden.

### 2.7 PDF-Erstellung

Die Brotzeitliste wird als PDF lokal auf dem Gerät erzeugt. Sie verlässt das Gerät nur, wenn sie aktiv geteilt wird (z. B. per AirDrop, E-Mail oder Drucken).

---

## 3. Verwendete Dienste Dritter

### Google Firebase (Firestore, Authentication, App Check)

Die App nutzt Google Firebase (Anbieter: Google Ireland Limited, Dublin) für die Datensynchronisation zwischen den Geräten des Hortes, die Anmeldung und App Check. Google verarbeitet die Daten im Auftrag; eine Übermittlung in die USA ist dabei nicht ausgeschlossen und erfolgt auf Grundlage des EU-US Data Privacy Framework bzw. von Standardvertragsklauseln. Die Firestore-Datenbank liegt in der **EU-Region »eur3«** (Rechenzentren in Belgien und den Niederlanden).

- Datenschutzinformationen von Google/Firebase: https://firebase.google.com/support/privacy

### Apple (App Attest, App Store, TestFlight)

App Attest ist ein Dienst von Apple. Bei der Verteilung über den App Store und TestFlight kann Apple eigene Daten erheben (z. B. Absturzberichte oder Feedback der Testpersonen). Hierfür gilt die Datenschutzrichtlinie von Apple: https://www.apple.com/de/legal/privacy/

Die App nutzt **keine** Analyse-, Werbe- oder Tracking-Dienste.

---

## 4. Nicht erhobene Daten

Die App erhebt **keine** der folgenden Daten:

- Nachnamen, Geburtsdaten, Adressen oder Kontaktdaten von Kindern oder Eltern
- Gesundheitsdaten (z. B. Allergien)
- Kamera, Fotos oder Mikrofon
- Standortdaten
- Kontakte oder Kalender
- Biometrische Daten
- Werbe- oder Tracking-Kennungen

---

## 5. Datenweitergabe an Dritte

Es werden **keine personenbezogenen Daten verkauft, für Werbung genutzt oder an Dritte weitergegeben**. Die Synchronisation über Firebase dient ausschließlich der internen Nutzung im Hort; Google verarbeitet die Daten dabei als technischer Dienstleister.

---

## 6. Datensicherheit

- Die Übertragung zwischen App und Firebase erfolgt verschlüsselt (TLS).
- Zugriffe auf die Datenbank erfordern die Anmeldung mit einem vom Hort freigeschalteten Konto und werden zusätzlich über App Check abgesichert.
- Der Team-Bereich auf den Hort-iPads ist durch eine PIN geschützt.
- Lokal gespeicherte Daten liegen im geschützten Speicherbereich der App und werden von iOS verschlüsselt.

---

## 7. Speicherdauer und Löschung

Die Daten bleiben gespeichert, bis das Hortteam sie in der App löscht:

- Verlässt ein Kind den Hort, wird sein Name in den Einstellungen entfernt.
- Wird eine Brotzeit gelöscht, werden auch alle zugehörigen Einträge gelöscht. Einträge vergangener Brotzeiten bleiben bis dahin erhalten.

Mit dem Löschen der App werden die lokal gespeicherten Daten auf dem jeweiligen Gerät entfernt; die Daten der anderen Hort-Geräte und in Firebase bleiben davon unberührt.

---

## 8. Rechte der Betroffenen

Eltern bzw. betroffene Personen haben das Recht auf Auskunft, Berichtigung, Löschung und Einschränkung der Verarbeitung ihrer Daten sowie ein Widerspruchsrecht. Anfragen bitte an das Hortteam oder an die unten genannte Kontaktadresse.

Außerdem besteht ein Beschwerderecht bei einer Datenschutz-Aufsichtsbehörde, in Bayern beim Bayerischen Landesamt für Datenschutzaufsicht (BayLDA).

---

## 9. Verbreitung und Nutzerkreis

Die App wird über den App Store als nicht öffentlich auffindbare App („Unlisted App“, nur per Link) sowie über Apple TestFlight an das Hortteam und auf die Hort-iPads verteilt. Ohne Konto des Horts ist sie nicht nutzbar.

---

## 10. Kontakt

Bei Fragen zum Datenschutz wenden Sie sich bitte an:

**Martin Zanker**  
E-Mail: martinzankerdevelopment@gmail.com
