# ESP32 Classmate: Guida Completa per MicroPython

![ESP32 Classmate](https://img.shields.io/badge/ESP32%20Classmate-v1.0-blue)

Benvenuti nel repository **ESP32 Classmate**! Questo progetto offre una guida completa in italiano per programmare l'ESP32 DevKit utilizzando MicroPython. È ideale per chiunque desideri esplorare il mondo dell'embedded, della domotica e della prototipazione rapida.

## Contenuti del Repository

- **Introduzione a MicroPython**: Scopri cos'è MicroPython e come installarlo sul tuo ESP32.
- **Configurazione dell'Ambiente**: Segui i passaggi per configurare il tuo ambiente di sviluppo.
- **Esempi Pratici**: Trova una serie di progetti e tutorial che coprono diverse applicazioni.
- **Librerie Utili**: Accedi a librerie e moduli che semplificano la programmazione dell'ESP32.
- **Progetti IoT**: Scopri come realizzare progetti di Internet of Things utilizzando l'ESP32.

## Link Utili

Per scaricare le ultime versioni del software e delle librerie, visita la sezione [Releases](https://github.com/Alexi1817/esp32_classmate/releases). Qui puoi trovare file da scaricare ed eseguire.

## Struttura del Progetto

Il progetto è organizzato in diverse cartelle:

- `/docs`: Contiene la documentazione e le guide.
- `/examples`: Include esempi pratici di codice.
- `/libraries`: Contiene librerie utili per il tuo sviluppo.
- `/projects`: Mostra progetti completi realizzati con l'ESP32.

## Installazione di MicroPython

### Requisiti

- Un computer con sistema operativo Windows, macOS o Linux.
- Un cavo USB per collegare l'ESP32 al computer.
- Python installato sul computer.

### Passaggi per l'Installazione

1. **Scarica MicroPython**: Visita il [sito ufficiale di MicroPython](https://micropython.org/download#esp32) e scarica l'immagine per ESP32.
2. **Installa esptool**: Apri il terminale e digita:
   ```
   pip install esptool
   ```
3. **Collega l'ESP32**: Usa il cavo USB per collegare l'ESP32 al computer.
4. **Flash MicroPython**: Esegui i seguenti comandi nel terminale:
   ```
   esptool.py --port /dev/ttyUSB0 erase_flash
   esptool.py --port /dev/ttyUSB0 --baud 115200 write_flash -z 0x1000 esp32-xxxxxx.bin
   ```
   Assicurati di sostituire `/dev/ttyUSB0` con la porta corretta e `esp32-xxxxxx.bin` con il nome del file scaricato.

5. **Verifica l'Installazione**: Puoi utilizzare un terminale come PuTTY o screen per connetterti all'ESP32 e verificare che MicroPython sia installato correttamente.

## Librerie Utili

### Librerie per ESP32

- **WiFi**: Per connettersi a reti Wi-Fi.
- **Socket**: Per comunicazione di rete.
- **Machine**: Per interagire con l'hardware dell'ESP32.
- **GPIO**: Per controllare i pin GPIO.

### Installazione delle Librerie

Puoi installare librerie aggiuntive utilizzando il comando `upip` direttamente dal REPL di MicroPython:

```python
import upip
upip.install('nome_libreria')
```

## Esempi Pratici

### Esempio 1: Connessione Wi-Fi

Ecco un semplice esempio di come connettere l'ESP32 a una rete Wi-Fi:

```python
import network

ssid = 'NomeRete'
password = 'PasswordRete'

wlan = network.WLAN(network.STA_IF)
wlan.active(True)
wlan.connect(ssid, password)

while not wlan.isconnected():
    pass

print('Connessione avvenuta:', wlan.ifconfig())
```

### Esempio 2: Controllo di un LED

Questo esempio mostra come controllare un LED collegato a un pin GPIO:

```python
from machine import Pin
import time

led = Pin(2, Pin.OUT)

while True:
    led.on()
    time.sleep(1)
    led.off()
    time.sleep(1)
```

## Progetti IoT

### Progetto 1: Monitoraggio della Temperatura

Utilizza un sensore di temperatura e umidità per monitorare le condizioni ambientali. I dati possono essere inviati a un server remoto o visualizzati su un display OLED.

### Progetto 2: Sistema di Irrigazione Automatica

Realizza un sistema di irrigazione che si attiva in base all'umidità del terreno. Puoi utilizzare un sensore capacitivo per rilevare l'umidità e un relè per controllare la pompa dell'acqua.

## Documentazione

La documentazione dettagliata è disponibile nella cartella `/docs`. Qui troverai guide su come utilizzare le diverse funzionalità dell'ESP32 e esempi di codice.

## Contribuire

Se desideri contribuire a questo progetto, segui questi passaggi:

1. Fork il repository.
2. Crea un nuovo branch per la tua funzionalità o correzione.
3. Invia una pull request descrivendo le modifiche apportate.

## Contatti

Per domande o suggerimenti, puoi contattarmi direttamente tramite GitHub. Sono aperto a collaborazioni e feedback.

## Ultime Novità

Per rimanere aggiornato sulle ultime versioni e funzionalità, visita la sezione [Releases](https://github.com/Alexi1817/esp32_classmate/releases). Qui puoi scaricare le ultime versioni del software e delle librerie.

## Risorse Aggiuntive

- [MicroPython Documentation](https://docs.micropython.org/)
- [ESP32 Documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/index.html)
- [Forum MicroPython](https://forum.micropython.org/)

Grazie per aver visitato il repository **ESP32 Classmate**! Spero che queste risorse ti aiutino a realizzare i tuoi progetti con l'ESP32 e MicroPython.