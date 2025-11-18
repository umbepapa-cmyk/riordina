Agente di Riordino File con IA

Questo script Python automatizza l'organizzazione e la rinomina dei file in una cartella specificata utilizzando l'intelligenza artificiale di Google Gemini.

Funzionalità

Analisi Testuale: Legge e comprende il contenuto di PDF, DOCX, TXT e fogli Excel.

Visione Artificiale: "Guarda" le immagini (PNG, JPG, ecc.) per generare titoli descrittivi basati sul contenuto visivo.

Rinomina Automatica: Rinomina i file con titoli chiari, concisi e in italiano, eliminando codici oscuri.

Sicurezza: Utilizza variabili d'ambiente per proteggere la chiave API.

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
