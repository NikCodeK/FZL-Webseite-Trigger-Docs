# Password Protection TODO

## 🔐 **Password Protection für F&E Website**

### **Ziel:**
Sicherheits-Popup implementieren, das die Website blockiert bis das richtige Passwort eingegeben wird.

### **Features zu implementieren:**

#### **1. Password Popup beim Seitenstart:**
- [ ] Modal Overlay das die ganze Seite blockiert
- [ ] Passwort-Eingabefeld mit "Enter" zum Bestätigen
- [ ] "Zugang verweigert" Meldung bei falschem Passwort
- [ ] Nur bei richtigem Passwort wird die Seite freigegeben

#### **2. Sicherheits-Features:**
- [ ] Passwort im Code (für einfache Verwaltung)
- [ ] Session Storage - Passwort bleibt für die Session gespeichert
- [ ] Keine URL-Parameter - Passwort nicht in der URL sichtbar
- [ ] Einfaches Design - passt zum Rest der Seite

#### **3. Technische Umsetzung:**
- [ ] JavaScript Password Check beim `DOMContentLoaded`
- [ ] CSS Modal mit Overlay
- [ ] Passwort-Vergleich mit hardcoded Wert
- [ ] Session Storage für "bereits authentifiziert"

#### **4. Passwort-Optionen:**
- [ ] Passwort festlegen (z.B. "F&E2024" oder firmen-spezifisch)
- [ ] Passwort im Code oder in separater Konfiguration
- [ ] Optional: "Passwort vergessen" Funktion

### **Code-Struktur:**
```html
<!-- Password Modal -->
<div id="passwordModal" class="password-modal">
    <div class="password-content">
        <h2>Zugang erforderlich</h2>
        <input type="password" id="passwordInput" placeholder="Passwort eingeben">
        <button id="passwordSubmit">Zugang gewähren</button>
        <div id="passwordError" class="error-message"></div>
    </div>
</div>
```

```javascript
// Password Check
const CORRECT_PASSWORD = "F&E2024"; // Zu definieren
const PASSWORD_KEY = "fe_authenticated";

// Check if already authenticated
if (sessionStorage.getItem(PASSWORD_KEY) !== "true") {
    showPasswordModal();
}
```

### **CSS für Modal:**
```css
.password-modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    z-index: 9999;
    display: flex;
    align-items: center;
    justify-content: center;
}
```

### **Status:**
- [ ] **Nicht implementiert** - für zukünftige Entwicklung
- [ ] **Priorität:** Niedrig (Website funktioniert bereits)
- [ ] **Aufwand:** 1-2 Stunden

### **Notizen:**
- Passwort sollte einfach aber sicher sein
- Session Storage verhindert mehrfache Eingabe pro Session
- Modal sollte responsive sein
- Fehlerbehandlung für falsche Passwörter
