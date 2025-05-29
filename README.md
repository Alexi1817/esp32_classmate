# Guida all uso di ESP32 DevKit con MicroPython 


## Installazione dei Driver 

Partiamo dai driver: 

## Windows 
Scaricate questi: 

- https://sparks.gogo.co.nz/ch340.html
- https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers

## Linux 
- Gia presenti

## MacOS 
Scaricate questi: 
- https://www.silabs.com/developer-tools/usb-to-uart-bridge-vcp-drivers

## Installazione su Windows 

- Installate CH340
- Seguite i procedimenti di quando aprite exe
- Per CP210x dobbiamo fare un paio di procedimenti in piu'
- Premente WIN + R
- Scrivete: devmgmt.msc
- Espandi la sezione Altri Dispostivi o Porte (COM e LPT)
- Cerca una di queste:
    - USB2.0-Serial
    - Dispositivo sconosciuto
    - CP2102
    - CP210x USB to UART Bridge
- Premi il tasto destro aggiorna il driver
- Ora Cerca i driver sul computer
- Seleziona la cartella che hai estratto dal file zip CP210x_Universal
- Adesso dovresti avere Silicon Labs CP210x USB to UART Bridge
- Riavvia


## Installazione su MacOS

- Aprite il file .dmg che avete scaricato e installatelo
- Riavvia

## Thonny IDE

- Da questo link https://thonny.org/
- Scaricate IDE in base al vostro OS
- Installatelo
- Apritelo
- Collegate la vostra ESP32
- Andate su Tools > Options
- Tab Interpreter
- Selezionate MicroPython Esp32
- Poi sulla Port e selezionate la Serial Bus
- Premete Ok
- Ora dovreste avere collegato ESP32 al IDE
- Andate in View
- Premete Files
- Se tutto è andato in maniera corretta dovreste vedere boot.py


## Flashare il firmware 

- Aprite Thonny
- Andare in Tool > Options > Interpreter
- In basso a destra c'è Install or Update MicroPython
- Qui ci sono due strade la prima che lo fate fare in automatico da Thonny
- In alternativa andate https://micropython.org/download/ESP32_GENERIC/
- Scriate l'ultima versione(File .bin)
- Ritornate su Thonny
- Ci sono tre linee vicino Install in basso a destra
- Premete e andate su Select Local Mircopython Image





  
