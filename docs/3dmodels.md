### Descrizione del Database `3dmodels`

Il database `3dmodels` è progettato per gestire e organizzare modelli 3D di vari organi umani, senza limitarsi a un singolo tipo. Questo database è utile in tutti i contesti in cui è necessario archiviare e accedere a modelli 3D dettagliati di diversi organi.

#### Struttura Generale
- **Nome del Database:** `3dmodels`
- **Codifica Caratteri:** UTF-8, che supporta una vasta gamma di caratteri internazionali e simboli, ideale per nomi e descrizioni accurate.
- **Motore di Memorizzazione:** Utilizza InnoDB, che supporta transazioni sicure e garantisce l'integrità dei dati.

#### Tabelle Principali (Esempio: `organ_models`)

Il database può contenere diverse tabelle simili per ciascun organo, che possono essere strutturate in maniera standard. Ecco un esempio di come potrebbe essere una tabella generica, chiamata `organ_models`:

- **`model_id`**: Un identificatore univoco per ogni modello, generato automaticamente.
- **`model_name`**: Il nome del modello, ad esempio "Cuore", "Fegato", "Polmone", con un massimo di 100 caratteri.
- **`model_description`**: Una descrizione del modello, come "Modello dettagliato del cuore umano con texture arteriose".
- **`file_type`**: Il formato del file 3D, ad esempio STL, OBJ, FBX, che specifica il tipo di file utilizzato.
- **`textures_folder_path`**: Il percorso della cartella che contiene le texture associate al modello, utile per visualizzazioni più realistiche.
- **`created_at`**: La data e l'ora in cui il modello è stato creato.
- **`updated_at`**: La data e l'ora dell'ultimo aggiornamento, utile per tenere traccia delle modifiche nel tempo.

#### Caratteristiche del Database

- **Generalizzazione per Ogni Organo**: Sebbene l'esempio riportato faccia riferimento a modelli di cuori, il database è strutturato per essere flessibile e ospitare modelli di vari organi. 
- **Espandibilità**: Nuove tabelle possono essere aggiunte per diversi tipi di organi, mantenendo una struttura coerente per facilitare la gestione dei dati.
- **Supporto per Texture e Dettagli Aggiuntivi**: L'inclusione di percorsi per le texture consente di associare file di texture specifici per una visualizzazione realistica dei modelli 3D.