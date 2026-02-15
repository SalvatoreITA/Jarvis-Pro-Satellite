# 🎙️ Jarvis Pro - Firmware Precompilato

[![it](https://img.shields.io/badge/lang-it-green.svg)](https://github.com/SalvatoreITA/Jarvis-Pro-Satellite/blob/main/README_it.md)
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/SalvatoreITA/Jarvis-Pro-Satellite/blob/main/README.md)

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
[![version](https://img.shields.io/badge/version-1.0.0-blue.svg)]()
[![maintainer](https://img.shields.io/badge/maintainer-Salvatore_Lentini_--_DomHouse.it-green.svg)](https://www.domhouse.it)

**Jarvis Pro** è un firmware personalizzato per **ESP32-S3** che trasforma il tuo dispositivo in un satellite vocale avanzato per Home Assistant.

Questo progetto è un fork ottimizzato di [Kristopher Mackowiak](https://github.com/KristopherMackowiak/ha_voice_assistant), arricchito con funzionalità esclusive per il debug e una migliore esperienza utente.

> **⚠️ Nota:** In questo repository trovi il file `.bin` precompilato. Non serve installare ESPHome o compilare codice. Basta flasharlo!

## 📚 Guida Completa:
Trovi la guida dettagliata sul sito: [ddddddd](https://github.com/KristopherMackowiak/ha_voice_assistant),

## ✨ Novità "Jarvis Pro"

Rispetto al progetto originale, questa versione include:

* 📝 **Debug Vocale:** Sensori esclusivi su Home Assistant che mostrano il testo di **cosa hai detto** e **cosa ha risposto** l'AI (fondamentale per capire se il microfono capisce bene).
* 📶 **Diagnostica WiFi:** Nuovi sensori per monitorare potenza segnale (dB/%) e Indirizzo IP.
* 🔘 **Pulsante "Forza Ascolto":** Un bottone virtuale su Home Assistant per attivare il microfono senza usare la wake word.
* 🇮🇹 **Ottimizzazione Italiana:** Wake word e timer pre-configurati per rispondere meglio ai comandi in italiano.
* 🔊 **Nuovi Suoni:** Feedback sonori aggiuntivi per errori di connessione o scadenza cloud.
* 🆘 **Access Point di Emergenza:** Se non trova il WiFi, dopo 60 secondi crea una rete `Voice Assistant` per configurarlo col telefono.

## 🚀 Come Installare

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

## ⚠️ Disclaimer (Esclusione di Responsabilità)

L'utilizzo di questo file binario (`.bin`) implica l'accettazione dei seguenti termini:

### 1. Fornitura "Così com'è" (As-Is)
Il presente firmware viene fornito **"così com'è"**, senza garanzie di alcun tipo, esplicite o implicite, incluse, a titolo esemplificativo, garanzie di commerciabilità o idoneità a uno scopo specifico. L'autore non garantisce che le funzioni contenute nel firmware soddisfino le esigenze dell'utente o che il funzionamento sia privo di errori.

### 2. Assunzione del Rischio
L'installazione di firmware non ufficiali o modificati comporta rischi intrinseci. L'utente si assume la **piena e totale responsabilità** per qualsiasi operazione di "flashing" o caricamento del firmware sul proprio hardware.

### 3. Esclusione di Responsabilità per Danni
In nessun caso l'autore potrà essere ritenuto responsabile per qualsiasi danno diretto, indiretto, incidentale o consequenziale, inclusi, ma non limitati a:

* **Danni all'hardware:** Blocco irreversibile del dispositivo (*brick*), surriscaldamento o rottura di componenti.
* **Perdita di dati:** Perdita di configurazioni o informazioni memorizzate sul dispositivo o sui sistemi connessi (es. Home Assistant).
* **Malfunzionamenti:** Errori di rete, vulnerabilità di sicurezza o comportamenti imprevisti del dispositivo.

### 4. Nessun Obbligo di Supporto
L'autore, pur avendo apportato migliorie e fix al progetto originale, **non ha alcun obbligo** di fornire supporto tecnico, aggiornamenti o correzioni future.

### 5. Relazione con il Progetto Originale
Questo firmware è una versione indipendente e modificata. **Non è approvato, sponsorizzato o supportato** dall'autore del progetto originale né dai creatori di ESPHome.

## ❤️ Crediti
* **Sviluppo Originale:** [Kristopher Mackowiak](https://github.com/KristopherMackowiak/ha_voice_assistant)
* **Modifiche:** [Salvatore Lentini](https://domhouse.it)
* **Tecnologia:** Basato su [ESPHome](https://esphome.io) e [microWakeWord](https://github.com/kahrendt/microWakeWord).

