# 🚀 Guida all'Uso di ESP32 DevKit con MicroPython

> Una guida completa e **in italiano** per iniziare con l'ESP32 DevKit v1 (WROOM-32) e programmare in MicroPython. Include installazione driver, setup di Thonny IDE, flashing del firmware.

## 🧰 Requisiti

* ESP32 DevKit v1 (con chip ESP32-WROOM-32)
* Cavo USB **dati** (non solo ricarica!)
* PC con Windows, macOS o Linux
* Connessione Internet

---

## 📦 Installazione dei Driver

### 🪟 Windows

Scarica entrambi i driver, a seconda del chip sulla tua scheda (CH340 o CP210x):

* 🧲 [CH340 Driver](https://sparks.gogo.co.nz/ch340.html)
* 🧲 [CP210x Driver](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers)

Dopo averli scaricati:

1. Installa CH340 normalmente.
2. Per CP210x:

   * Premi `WIN + R` → digita `devmgmt.msc` → Invio
   * In **Gestione dispositivi**, trova la voce tipo:

     * `USB2.0-Serial`
     * `Dispositivo sconosciuto`
     * `CP2102` o `CP210x USB to UART Bridge`
   * Tasto destro → **Aggiorna driver**
   * Scegli "Cerca il software nel computer"
   * Seleziona la cartella dove hai estratto il `.zip` del CP210x
   * Dopo l'installazione, **riavvia il PC**

### 🍎 macOS

* Scarica e installa: [CP210x macOS VCP Driver](https://www.silabs.com/developer-tools/usb-to-uart-bridge-vcp-drivers)
* Apri il `.dmg` → esegui `.pkg`
* Riavvia il Mac

### 🐧 Linux

* I driver sono **già inclusi nel kernel**
* Se necessario, aggiungi l'utente al gruppo `dialout`:

  ```bash
  sudo usermod -a -G dialout $USER
  ```

  Poi **riavvia** il PC.

---

## 🧠 Installazione e Configurazione di Thonny IDE

### 💾 Scarica Thonny

* Sito ufficiale: [https://thonny.org](https://thonny.org)
* Scegli la versione per il tuo sistema operativo

### ⚙️ Configura Thonny

1. Apri Thonny
2. Collega la tua ESP32 via USB
3. Vai su: `Tools > Options > Interpreter`
4. Scegli:

   * Interpreter: **MicroPython (ESP32)**
   * Port: seleziona la porta (es. COM3, /dev/ttyUSB0, ecc.)
5. Clicca **OK**
6. Vai su `View > Files`

   * Se vedi `boot.py`, la connessione è riuscita ✅

📸 ![Thonny Configuration](https://user-images.githubusercontent.com/123123/thonny-esp32-setup.png)

---

## 💾 Flash del Firmware MicroPython

### Opzione 1 – Automatico con Thonny

1. `Tools > Options > Interpreter`
2. In basso a destra clicca **"Install or update MicroPython"**
3. Segui le istruzioni a schermo

### Opzione 2 – Manuale

1. Vai su: [https://micropython.org/download/ESP32\_GENERIC/](https://micropython.org/download/ESP32_GENERIC/)
2. Scarica l'ultima versione (`.bin`)
3. In Thonny: `Tools > Options > Interpreter`
4. In basso clicca le tre linee > **"Select local MicroPython image"**
5. Seleziona il file `.bin` scaricato
6. Segui le istruzioni per il flash

📸 ![Flash Firmware](https://user-images.githubusercontent.com/123123/thonny-flash.png)


---

## 📡 Contatti e Link

* 🌐 [jate.wtf](https://jate.wtf)
* 🐙 GitHub: [github.com/jate](https://github.com/jate)

---

