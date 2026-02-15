# 🎙️ Jarvis Pro - Firmware Precompilato

[![it](https://img.shields.io/badge/lang-it-green.svg)](https://github.com/SalvatoreITA/Jarvis-Pro-Satellite/blob/main/README_it.md)
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/SalvatoreITA/Jarvis-Pro-Satellite/blob/main/README.md)

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
[![version](https://img.shields.io/badge/version-1.0.o-blue.svg)]()
[![maintainer](https://img.shields.io/badge/maintainer-Salvatore_Lentini_--_DomHouse.it-green.svg)](https://www.domhouse.it)

<div align="center">
  <img src="https://github.com/SalvatoreITA/Telegram-Custom-Bot/blob/main/icon.png?raw=true" alt="Logo" width="150">
</div>

**Jarvis Pro** è un firmware personalizzato per **ESP32-S3** che trasforma il tuo dispositivo in un satellite vocale avanzato per Home Assistant.

Questo progetto è un fork ottimizzato di [ha_voice_assistant di Kristopher Mackowiak](https://github.com/KristopherMackowiak/ha_voice_assistant), arricchito con funzionalità esclusive per il debug e una migliore esperienza utente.

> **⚠️ Nota:** In questo repository trovi il file `.bin` precompilato. Non serve installare ESPHome o compilare codice. Basta flasharlo!

## ✨ Novità "Jarvis Pro"

Rispetto al progetto originale, questa versione include:

* 📝 **Debug Vocale:** Sensori esclusivi su Home Assistant che mostrano il testo di **cosa hai detto** e **cosa ha risposto** l'AI (fondamentale per capire se il microfono capisce bene).
* 📶 **Diagnostica WiFi:** Nuovi sensori per monitorare potenza segnale (dB/%) e Indirizzo IP.
* 🔘 **Pulsante "Forza Ascolto":** Un bottone virtuale su Home Assistant per attivare il microfono senza usare la wake word.
* 🇮🇹 **Ottimizzazione Italiana:** Wake word e timer pre-configurati per rispondere meglio ai comandi in italiano.
* 🔊 **Nuovi Suoni:** Feedback sonori aggiuntivi per errori di connessione o scadenza cloud.
* 🆘 **Access Point di Emergenza:** Se non trova il WiFi, dopo 60 secondi crea una rete `Voice Assistant` per configurarlo col telefono.

## 🛠️ Hardware Supportato

Questo firmware è compilato specificamente per **ESP32-S3** con questa configurazione PIN:

| Componente | Pin (GPIO) |
| :--- | :--- |
| **Microfono (I2S)** | WS=14, SCK=13, SD=15 |
| **Speaker (I2S)** | LRC=7, BCLK=8, DIN=10 |
| **LED Ring** | GPIO 21 |

## 🚀 Come Installare (Facile)

Non serve saper programmare. Segui questi passi:

1.  **Scarica il file:** Scarica il file `jarvis-pro.bin` dalla sezione [Releases](link-alle-tue-release) di questo repository.
2.  **Collega l'ESP32:** Attacca il tuo ESP32-S3 al computer via USB.
3.  **Usa ESPHome Web:**
    * Vai su [web.esphome.io](https://web.esphome.io/).
    * Clicca su **Connect** e seleziona la porta COM del tuo dispositivo.
    * Clicca su **Install**.
    * Seleziona il file `.bin` che hai appena scaricato.
    * Clicca **Install** e aspetta che finisca.

### 4. Configurazione WiFi
Al primo avvio, il dispositivo dopo 60 secondi, creerà una rete WiFi chiamata **"Voice Assistant"**.
1.  Collegati a quella rete col telefono (Password: `1234567890` se richiesta, o nessuna).
2.  Collegati all'indirizzo: http://192.168.4.1
4.  Inserisci il nome (SSID) e la Password del tuo WiFi di casa.
5.  Salva. Il dispositivo si riavvierà e si collegherà alla rete.

## ⚙️ Integrazione in Home Assistant

Una volta connesso al WiFi:
1.  Apri Home Assistant.
2.  Troverai una notifica: **"Nuovo dispositivo scoperto"**.
3.  Clicca su **Configura** e segui i passaggi.
4.  Vai nelle impostazioni del dispositivo e abilita i nuovi sensori di debug.

## 📄 Crediti e Licenza

* **Sviluppo Originale:** [Kristopher Mackowiak](https://github.com/KristopherMackowiak/ha_voice_assistant)
* **Modifiche:** Salvatore Lentini
* **Tecnologia:** Basato su [ESPHome](https://esphome.io) e [microWakeWord](https://github.com/kahrendt/microWakeWord).

## ⚖️ Limitazione di Responsabilità

IN NESSUN CASO L'AUTORE O I DETENTORI DEL COPYRIGHT SARANNO RESPONSABILI PER QUALSIASI RECLAMO, DANNO O ALTRA RESPONSABILITÀ, SIA IN UN'AZIONE DI CONTRATTO, ILLECITO O ALTRO, DERIVANTE DA, O IN CONNESSIONE CON IL SOFTWARE O L'USO O ALTRE OPERAZIONI NEL SOFTWARE.

L'UTENTE SI ASSUME LA PIENA RESPONSABILITÀ PER:
* LA CONFIGURAZIONE DELL'HARDWARE ESP32.
* I COLLEGAMENTI ELETTRICI DEI COMPONENTI (MICROFONI, SPEAKER, LED).
* L'USO DEL DISPOSITIVO IN AMBIENTE DOMESTICO.

IL FIRMWARE VIENE DISTRIBUITO A SCOPO EDUCATIVO E DI TEST. NON È UN PRODOTTO CERTIFICATO PER USO COMMERCIALE O DI SICUREZZA CRITICA.
