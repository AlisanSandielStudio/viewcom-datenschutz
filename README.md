# viewcom-datenschutz
Datenschutzerklärung, Nutzungsbedingungen und Konto-löschen-Seite für ViewCom (iOS, Android und Web).

## Live: Teil der Web-App (seit dem Web-Start, Nov 2026)
- https://viewcom.sandiel.studio/datenschutz
- https://viewcom.sandiel.studio/nutzungsbedingungen
- https://viewcom.sandiel.studio/konto-loeschen
- Startseite https://viewcom.sandiel.studio/ ist jetzt die **Web-App**.

Quelle der Texte bleibt der Ordner **`site/`** in diesem Repo. Ausgeliefert werden sie
aber von **`viewcom-web`**: Die Domain hat nur eine Firebase-Hosting-Seite, und ein
Deploy ersetzt immer die komplette Seite. Deshalb:

1. Text hier in `site/` ändern, committen, pushen.
2. Im Repo `viewcom-web`:
   ```
   npm run sync-legal -- /Volumes/Volume1/viewcom-datenschutz/site
   npm run build
   firebase deploy --only hosting
   ```

**Aus diesem Repo NICHT mehr deployen** – das würde die Web-App überschreiben.
`firebase.json` zeigt deshalb auf ein Hosting-Ziel, das es absichtlich nicht gibt;
`firebase deploy` bricht hier mit „target … not configured“ ab.

## Alt: GitHub Pages
`index.html` und `nutzungsbedingungen.html` im Repo-Hauptordner sind die alten
GitHub-Pages-Seiten (Android 0.8 verlinkt noch dorthin). Sie werden durch
Weiterleitungen auf viewcom.sandiel.studio ersetzt, sobald die Domain live ist.
Das Repo muss öffentlich bleiben, bis keine App-Version mehr auf GitHub Pages verlinkt.
