Agente di Riordino File con IA

Questo script Python automatizza l'organizzazione e la rinomina dei file in una cartella specificata utilizzando l'intelligenza artificiale di Google Gemini.

Funzionalità

Analisi Testuale: Legge e comprende il contenuto di PDF, DOCX, TXT e fogli Excel.
  - **PDF Robusto**: Utilizza un doppio metodo di estrazione (pdfplumber + pypdfium2) per massimizzare la compatibilità con diversi tipi di PDF
  - **Rilevamento PDF Immagine**: Identifica automaticamente i PDF basati su immagini (documenti scannerizzati senza OCR)
  - **Codifiche Multiple**: Supporta diverse codifiche per file TXT (utf-8, latin-1, cp1252, iso-8859-1)

Visione Artificiale: "Guarda" le immagini (PNG, JPG, ecc.) per generare titoli descrittivi basati sul contenuto visivo.

Rinomina Automatica: Rinomina i file con titoli chiari, concisi e in italiano, eliminando codici oscuri.

Sicurezza: Utilizza variabili d'ambiente per proteggere la chiave API.

Gestione Errori Migliorata: Messaggi informativi che spiegano perché un file non può essere elaborato.

Requisiti

Python 3.x

Una chiave API di Google Gemini (AI Studio)

Installazione

Clona il repository:

git clone [https://github.com/TuoUtente/AgenteRiordino.git](https://github.com/TuoUtente/AgenteRiordino.git)


Crea un ambiente virtuale:

py -m venv .venv
.\.venv\Scripts\Activate


Installa le dipendenze:

pip install -r requirements.txt


Configurazione

Crea un file chiamato .env nella cartella principale del progetto.

Inserisci le seguenti variabili:

GEMINI_API_KEY="La_Tua_Chiave_API_Qui"
CARTELLA_DA_ESAMINARE="C:\Percorso\Della\Tua\Cartella"


Utilizzo

Esegui lo script principale:

python Riordina.py


Risoluzione Problemi

**PDF non interpretati correttamente**

Lo script usa un sistema a due livelli per estrarre testo dai PDF:

1. **Primo tentativo**: pdfplumber (metodo principale)
2. **Fallback automatico**: pypdfium2 (se pdfplumber fallisce)
3. **Identificazione PDF immagine**: Se nessun metodo trova testo, il PDF potrebbe essere basato su immagini (documento scannerizzato)

**Messaggi di errore comuni**

- `"PDF vuoto o senza pagine"`: Il file PDF non contiene pagine leggibili
- `"pypdfium2 non ha trovato testo (potrebbe essere un PDF basato su immagini)"`: Il PDF è probabilmente un documento scannerizzato senza OCR
- `"Impossibile decodificare il file TXT con le codifiche comuni"`: Il file TXT usa una codifica non standard

**Tipi di file supportati**

- **Documenti**: PDF, DOCX, TXT
- **Fogli di calcolo**: XLSX, XLS
- **Immagini**: PNG, JPG, JPEG, BMP, WEBP
