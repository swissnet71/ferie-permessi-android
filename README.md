# Ferie & Permessi – progetto Android

Prima versione del progetto Android nativo in Kotlin + Jetpack Compose.

## Funzioni incluse
- Saldi locali di ferie e ROL, espressi in ore.
- Configurazione indipendente della maturazione mensile.
- Recupero delle maturazioni arretrate all'apertura dell'app (utile se il telefono era spento il giorno 1).
- Registrazione delle ore utilizzate e storico movimenti.
- Rettifica manuale dei saldi.
- Persistenza locale tramite SharedPreferences; nessun account o server.

## Compilazione APK
1. Installa Android Studio (versione recente) e il JDK richiesto.
2. Apri questa cartella in Android Studio.
3. Attendi la sincronizzazione Gradle e installa Android SDK 35 se richiesto.
4. Seleziona **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. L'APK di debug sarà in `app/build/outputs/apk/debug/app-debug.apk`.

## Nota sul conteggio
L'app registra l'ultimo mese contabilizzato e applica ogni maturazione una sola volta. Le maturazioni vengono recuperate all'avvio, non tramite un processo garantito eseguito esattamente alle 00:00 del giorno 1: Android può sospendere le attività in background.

## Limiti di questa prima versione
- Non include ancora l'importazione/lettura OCR di PDF o foto delle buste paga: i valori della busta paga possono essere trascritti manualmente tramite rettifica saldi e configurazione.
- Non include ancora esportazione/backup esterno o calendario.
- La maturazione configurata viene applicata dal mese successivo all'ultimo mese contabilizzato; prima di usare l'app per i conteggi reali, imposta i saldi iniziali e le maturazioni mensili corrette.
- I dati sono memorizzati sul dispositivo. Disinstallando l'app o cancellando i dati dell'app, possono andare persi.
