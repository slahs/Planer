# 🎟️ Meine Tickets

Ein eleganter, persönlicher Ticket- & Aufgaben-Manager als **einzelne HTML-Datei**.
Läuft komplett im Browser – inklusive **Wiederholungen, Erinnerungen, Dark/Light-Mode** und optionalem **GitHub-Sync** über einen privaten Gist, damit du deine Tickets auf allen Geräten hast.

Installierbar als **PWA** (App-Symbol auf dem Homescreen, Offline-Betrieb, Browser-Benachrichtigungen).

---

## 🚀 In 3 Minuten auf GitHub Pages hosten

1. **Neues Repository** auf GitHub erstellen, z. B. `meine-tickets`.
2. Alle Dateien aus diesem Ordner hochladen (`index.html`, `manifest.webmanifest`, `sw.js`, `icons/` …).
3. Im Repo: **Settings → Pages → Source: `Deploy from a branch`** wählen, Branch `main` / Ordner `/ (root)` → **Save**.
4. Nach ~1 Minute ist deine App unter
   `https://<dein-user>.github.io/meine-tickets/` erreichbar.
5. Auf dem Handy im Browser öffnen → Menü → **„Zum Home-Bildschirm hinzufügen"** → fertig, sieht aus wie eine App.

> Tipp: Repo darf privat sein, wenn du **GitHub Pages Pro** hast. Sonst Repo öffentlich – die App enthält keinerlei Daten, deine Tickets liegen nur lokal & im privaten Gist.

---

## ☁️ GitHub-Sync (optional, empfohlen)

Damit deine Tickets auf allen Geräten verfügbar sind, kannst du sie automatisch in einen **privaten Gist** speichern.

### 1. Personal Access Token erstellen
- Öffne <https://github.com/settings/tokens?type=beta> („Fine-grained tokens").
- **Generate new token** → Name z. B. `tickets-sync`, Ablaufdatum nach Wunsch.
- **Account permissions → Gists → Read and write**.
- Token generieren und **kopieren** (er wird nur einmal angezeigt).

### 2. In der App einrichten
- Oben in der Toolbar auf **☁️ Sync** klicken.
- Token einfügen, **Gist-ID leer lassen** (wird beim ersten Upload automatisch angelegt).
- **„Automatisch synchronisieren"** anhaken → **Speichern** → **⬆️ Zum Gist speichern**.
- Die App speichert die neue **Gist-ID** automatisch.

### 3. Auf einem zweiten Gerät einrichten
- Dieselbe URL öffnen.
- **☁️ Sync** → Token + **gleiche Gist-ID** eintragen → **Speichern** → **⬇️ Vom Gist laden**.
- Ab jetzt synchronisieren sich beide Geräte automatisch (kurze Debounce nach jeder Änderung).

> Sicherheit: Token & Daten liegen ausschließlich in **deinem** Browser (localStorage) und in **deinem** privaten Gist. Niemand sonst kann darauf zugreifen.

---

## 🔔 Benachrichtigungen

- In der Toolbar auf **🔔** klicken und Berechtigung erlauben.
- Du bekommst eine Browser-/System-Benachrichtigung **15 Min. vor Fälligkeit**.
- **Wichtig:** Damit das im Hintergrund (App geschlossen) zuverlässig funktioniert, die App über **„Zum Home-Bildschirm hinzufügen"** als PWA installieren.
- Echte Server-Push-Notifications (Push, wenn der Browser komplett zu ist) wären nur mit einem externen Push-Server möglich – das ist hier bewusst nicht eingebaut, damit alles ohne Backend läuft.

---

## ⌨️ Tastenkürzel

| Taste | Aktion |
|------|--------|
| `N`  | Neues Ticket |
| `/`  | Suche fokussieren |
| `Esc`| Dialog schließen |

---

## 🔁 Wiederkehrende Tickets

Beim Anlegen eines Tickets unten **Wiederholung** wählen:
- **Täglich**, **Wöchentlich** (mit Wochentagen) oder **Monatlich**.
- Über **🔁 Serien** in der Toolbar kannst du eine Serie samt allen offenen Einträgen wieder löschen.

---

## 🛠️ Lokal ausführen

Einfach `index.html` doppelklicken. Für PWA/Service-Worker & Sync sollte sie aber über `http(s)://` geladen werden (z. B. GitHub Pages oder `python3 -m http.server`).

---

## 📄 Lizenz

MIT
