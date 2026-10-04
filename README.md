# Känguruh Starttimer

Starttimer für Känguruh-Regatten als Webapp und eigenständige App für Android und iOS.

## Funktionen

- Auswahl von Startzeiten für H-Boot anhand der Starttafel
- freier Countdown für Tests und/oder Anpassung an die Regatta-Uhr
- Countdown-Anzeige in **Minuten:Sekunden**
- Sprachansage bei 15 Minuten Restzeit bei Minutenwechsel
- In der letzten Minute Sprachansage alle xx Sekunden**

## Starten

```bash
npm install
npm run start
```

Für Web-Vorschau zusätzlich:

```bash
npx expo install react-dom react-native-web
npm run web
```

## Android- und iOS-App

Die nativen Installationsdateien werden mit [EAS Build](https://docs.expo.dev/build/introduction/) erstellt:

1. EAS CLI installieren oder per `npx` verwenden und anmelden: `npx eas-cli login`
2. Das Projekt einmalig mit einem Expo-Konto verknüpfen: `npx eas-cli init`
3. Vorschau-Build erstellen:

   ```bash
   npx eas-cli build --platform android --profile preview
   npx eas-cli build --platform ios --profile preview
   ```

   Android erzeugt eine installierbare APK. Für iOS wird ein internes Ad-hoc-Build erzeugt; zum Installieren muss das iPhone im Apple-Developer-Konto registriert sein.

Für die Veröffentlichung im Store:

```bash
npx eas-cli build --platform all --profile production
```

Der iOS-Store-Build erfordert eine Apple-Developer-Mitgliedschaft. Vor einer Veröffentlichung müssen die App-IDs `de.rawernic.kaenguruhstarttimer` in `app.json` durch eigene, noch nicht vergebene IDs ersetzt werden.
