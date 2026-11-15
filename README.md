# viewcom-datenschutz
Datenschutzerklärung, Nutzungsbedingungen und Konto-löschen-Seite für ViewCom (iOS, Android und Web).

## Live (seit G-4, Nov 2026): Firebase Hosting
- https://viewcom.sandiel.studio/datenschutz
- https://viewcom.sandiel.studio/nutzungsbedingungen
- https://viewcom.sandiel.studio/konto-loeschen
- Startseite https://viewcom.sandiel.studio/

Quelle ist der Ordner **`site/`**. Hochladen (im Repo-Ordner):

```
firebase deploy --only hosting
```

**Wichtig:** Die Web-App (`viewcom-web`) soll später unter derselben Domain laufen.
Ein Deploy ersetzt immer die komplette Seite. Sobald die Web-App live geht, ziehen
die Dateien aus `site/` nach `viewcom-web/public/` um, und dieses Repo deployt
nicht mehr auf Firebase.

## Alt: GitHub Pages
`index.html` und `nutzungsbedingungen.html` im Repo-Hauptordner sind die alten
GitHub-Pages-Seiten (Android 0.8 verlinkt noch dorthin). Sie werden durch
Weiterleitungen auf viewcom.sandiel.studio ersetzt, sobald die Domain live ist.
Das Repo muss öffentlich bleiben, bis keine App-Version mehr auf GitHub Pages verlinkt.
