# 📚 Book Recommender

Benvenuto nel progetto **Book Recommender**. Questa applicazione è un sistema client-server progettato per la gestione e la raccomandazione di libri, dotata di un'interfaccia grafica moderna.

Il sistema è composto da due moduli principali:
1.  **Server**: Gestisce la logica di business, le connessioni e l'interazione con il database.
2.  **Client**: Fornisce l'interfaccia utente (UI) per interagire con il sistema.

---

## 📋 Requisiti di Sistema

Per eseguire correttamente l'applicazione, assicurati di avere installato:

* **Java 21** (o versione superiore)
* **Maven** (installato e configurato nel PATH di sistema)
* **JavaFX** (gestito automaticamente dalle dipendenze Maven)

---

## 🚀 Guida all'Avvio Rapido

> **Nota Importante**: L'applicazione è fornita **già compilata** e pronta all'uso. Non è necessario eseguire la compilazione manuale prima dell'avvio.

### 🍎 Utenti macOS / 🐧 Linux

1.  Apri il Terminale e naviga nella cartella principale del progetto:
    ```bash
    cd /percorso/al/progetto/BookRecommender/BookRecommender-main
    ```

2.  Concedi i permessi di esecuzione agli script nella cartella `bin`:
    ```bash
    chmod +x bin/start-server.sh bin/start-client.sh
    ```

3.  **Avvia il Server** (in questa finestra del terminale):
    ```bash
    ./bin/start-server.sh
    ```

4.  Apri una **nuova finestra o scheda del Terminale** e avvia il Client:
    ```bash
    ./bin/start-client.sh
    ```

### 🪟 Utenti Windows

1.  Apri il Prompt dei comandi (`cmd`) o PowerShell e naviga nella cartella del progetto:
    ```cmd
    cd C:\percorso\al\progetto\BookRecommender\BookRecommender-main
    ```

2.  **Avvia il Server**:
    ```cmd
    bin\start-server.bat
    ```

3.  Apri una **nuova finestra del Prompt dei comandi** e avvia il Client:
    ```cmd
    bin\start-client.bat
    ```

*Suggerimento: Su Windows è possibile avviare gli script `.bat` anche facendo doppio clic direttamente da Esplora File.*

---

## 🛠 Risoluzione dei Problemi

### macOS / Linux
* **Errore "Permission denied"**: Assicurati di aver eseguito il comando `chmod +x bin/*.sh` come indicato nella guida.
* **Errore "mvn: command not found"**: Maven non è installato o non è nel PATH.
    * *Installazione via Homebrew (macOS)*: `brew install maven`
    * *Installazione via APT (Ubuntu/Debian)*: `sudo apt install maven`

### Windows
* **Errore "'mvn' non è riconosciuto..."**: Maven non è installato o la variabile d'ambiente PATH non è configurata correttamente. Verifica digitando `mvn -version` nel terminale.
* **La finestra non si apre**: Controlla il terminale per messaggi di errore e verifica la versione di Java con `java -version` (deve essere 21 o superiore).

### Note Generali
* **Problemi di Rendering**: Gli script sono configurati per utilizzare il renderer software (`-Dprism.order=sw`) per garantire la massima compatibilità grafica su tutti i sistemi.
* **Porte Occupate**: Se il server non parte, assicurati che la porta utilizzata non sia occupata da un altro processo.

---

## 💻 Stack Tecnologico

Il progetto è costruito utilizzando le seguenti tecnologie (basato sul file `pom.xml`):

* **Linguaggio**: Java 21
* **Interfaccia Utente**: JavaFX 21.0.2
* **Gestione Dipendenze**: Maven
* **Database**:
    * PostgreSQL (Driver 42.7.1)
    * H2 Database (In-memory fallback, ver 2.2.224)
* **Librerie UI Aggiuntive**:
    * ControlsFX 11.2.1
    * FormsFX 11.6.0
    * ValidatorFX 0.5.0
* **Testing**: JUnit 5.10.2

---

## 📂 Struttura del Progetto

```text
BookRecommender-main/
├── bin/
│   ├── start-client.sh    # Avvio Client (macOS/Linux)
│   ├── start-client.bat   # Avvio Client (Windows)
│   ├── start-server.sh    # Avvio Server (macOS/Linux)
│   └── start-server.bat   # Avvio Server (Windows)
├── src/                   # Codice sorgente Java e risorse
├── target/                # Artefatti compilati
├── db_credentials.properties # Configurazione credenziali DB
└── pom.xml                # Configurazione Maven e dipendenze
