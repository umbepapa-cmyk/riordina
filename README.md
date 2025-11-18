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

Crea un file chiamato .env nella cartella principale del progetto copiando il template fornito:

cp .env.example .env


Modifica il file .env con i tuoi valori:

Ottieni una chiave API gratuita di Google Gemini da: https://makersuite.google.com/app/apikey

Inserisci la tua chiave API e il percorso della cartella da esaminare nel file .env:

GEMINI_API_KEY=la_tua_chiave_api_qui
CARTELLA_DA_ESAMINARE=/percorso/completo/della/tua/cartella

Note:

Non utilizzare virgolette attorno ai valori

Utilizza percorsi assoluti per CARTELLA_DA_ESAMINARE

Il file .env non viene tracciato da git per proteggere la tua chiave API


Utilizzo

IMPORTANTE: Esegui lo script dalla cartella principale del progetto (dove si trova il file .env):

python Riordina.py
