# n8n Webhook Integration - To-Do Liste

## 🎯 Ziel
Die F&E-Antrag Website als funktionsfähigen n8n Webhook-Trigger einrichten.

## 📋 To-Do Liste

### Phase 1: n8n Workflow Setup
- [x] **1.1** n8n Webhook Node erstellen
- [x] **1.2** Webhook URL generieren und kopieren
- [x] **1.3** Workflow für F&E-Antrag Verarbeitung aufbauen
- [x] **1.4** Test-Webhook mit einfachen Daten testen ✅

### Phase 2: Frontend Konfiguration
- [x] **2.1** Webhook URL in JavaScript einsetzen
- [x] **2.2** JSON-Datenformat für n8n optimieren (Vereinfacht - nur technischer Erfolg)
- [x] **2.3** Request-Headers und Content-Type anpassen ✅
- [x] **2.4** Error Handling für Webhook-Calls verbessern ✅

### Phase 3: Datenstruktur & Validierung
- [ ] **3.1** Formulardaten strukturiert für n8n aufbereiten
- [ ] **3.2** Client-seitige Validierung erweitern
- [ ] **3.3** Timestamp und Metadaten hinzufügen
- [ ] **3.4** Input Sanitization implementieren

### Phase 4: Response Handling
- [ ] **4.1** n8n Response-Format definieren
- [ ] **4.2** Success/Error States richtig verarbeiten
- [ ] **4.3** Loading States und User Feedback verbessern
- [ ] **4.4** Download-Links oder Weiterleitungen handhaben

### Phase 5: Testing & Debugging
- [ ] **5.1** Webhook mit Test-Daten testen
- [ ] **5.2** Browser DevTools für Debugging nutzen
- [ ] **5.3** n8n Workflow Logs überprüfen
- [ ] **5.4** Error-Szenarien durchspielen

### Phase 6: Deployment & Zugänglichkeit
- [ ] **6.1** Website deployment (Vercel/Netlify/GitHub Pages)
- [ ] **6.2** Domain/URL für R&D Team
- [ ] **6.3** Zugriff testen
- [ ] **6.4** Team informieren

### Phase 7: Security & Polish
- [ ] **7.1** CSRF Protection (optional)
- [ ] **7.2** Rate Limiting implementieren (optional)
- [ ] **7.3** Final Testing mit echten Daten

## 🔧 Technische Details

### Aktuelle Webhook URL
```
https://cleverfunding.app.n8n.cloud/webhook-test/fe-antrag-upload
```

### Erwartetes Datenformat
```json
{
  "body": {
    "text": "Gesprächsprotokoll Inhalt...",
    "fileType": "transcript",
    "timestamp": "2024-01-01T12:00:00.000Z",
    "source": "web-interface"
  }
}
```

### Erwartete Response
```json
{
  "status": "success",
  "document": {
    "projekt": "Projektname",
    "drive_link": "https://drive.google.com/..."
  },
  "processing_time": "2.5s"
}
```

## 📝 Notizen
- Webhook URL muss in Zeile 274 der HTML-Datei ersetzt werden
- n8n Workflow sollte die eingehenden Daten verarbeiten und ein F&E-Dokument generieren
- Error Handling sollte benutzerfreundliche Meldungen anzeigen

## ✅ Status
- **Gestartet:** Heute
- **Aktueller Schritt:** Phase 3.1 - Formulardaten strukturiert für n8n aufbereiten
- **Nächster Schritt:** 3.1 - Datenstruktur optimieren
