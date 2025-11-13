# 🇮🇹 Guida Test FantaMatch - Manuale Completo

Ciao! Questo documento ti guiderà attraverso tutti i test per FantaMatch. Testa tutto con attenzione e segnala qualsiasi problema o suggerimento.

## 🚀 **Panoramica**

FantaMatch è un gioco di predizioni calcistiche in stile torneo dove:
- I giocatori scelgono squadre ad ogni turno
- Avanzano o vengono eliminati in base ai risultati
- Diversi preset modificano le regole di eliminazione
- L'obiettivo è essere l'ultimo giocatore rimasto

## 🌐 **Accesso al Sito**

**URL**: https://fantamatch.netlify.app

---

## 📋 **FASE 1: Test Iniziale & Login**

### 1.1 Landing Page
- [ ] Apri https://fantamatch.netlify.app
- [ ] Verifica che la pagina si carichi correttamente
- [ ] Controlla che tutto il testo sia in italiano
- [ ] Testa il cambio lingua (IT/EN) nell'angolo superiore
- [ ] Verifica che il design sia responsive (prova su mobile)

### 1.2 Login
- [ ] Clicca "Accedi" 
- [ ] Usa queste credenziali di test:
  - **Email**: `alekos@fantamatch.com`
  - **Password**: `Test01.!`
- [ ] Verifica che il login funzioni
- [ ] Dovresti essere reindirizzato alla dashboard

---

## 📊 **FASE 2: Dashboard e Navigazione**

### 2.1 Dashboard Principale
- [ ] Verifica che la dashboard si carichi
- [ ] Controlla le sezioni: Statistiche, Tornei, Attività Recente
- [ ] Testa la sidebar navigation (mobile e desktop)
- [ ] Verifica che tutte le traduzioni siano corrette
- [ ] Prova a cambiare lingua e torna all'italiano

### 2.2 Menu di Navigazione
- [ ] Testa tutti i link nella sidebar:
  - [ ] Dashboard
  - [ ] Tornei
  - [ ] (Altri link se presenti)
- [ ] Verifica che la navigazione mobile funzioni correttamente

---

## 🏆 **FASE 3: Creazione Tornei**

### 3.1 Accesso alla Creazione
- [ ] Vai a "Tornei" dalla sidebar
- [ ] Clicca "Crea Torneo" 
- [ ] Verifica che il form di creazione si apra

### 3.2 Form Creazione Torneo
- [ ] **Nome Torneo**: Inserisci "Test Serie A Championship"
- [ ] **Lega**: Seleziona "Serie A"
- [ ] **Preset**: Prova ogni preset (A, B, D, E)
  - [ ] Clicca l'icona "i" per leggere le regole
  - [ ] Verifica che le spiegazioni siano chiare
- [ ] **Giocatori Max**: Inserisci "20"
- [ ] **Timing**: Seleziona una data/settimana futura
- [ ] Clicca "Crea Torneo"

### 3.3 Verifica Creazione
- [ ] Dovrebbe apparire un modal di successo
- [ ] Copia il **Codice Invito** (formato: FNTA-2025-XXXXX)
- [ ] Clicca "Vai al Torneo"
- [ ] Verifica che ti porti alla pagina del torneo

---

## 🎮 **FASE 4: Test Pagina Torneo**

### 4.1 Pagina Torneo (Creatore)
- [ ] Verifica che vedi le informazioni del torneo
- [ ] Controlla la sezione "Azioni Torneo"
- [ ] Verifica il codice invito sia visibile
- [ ] Testa il pulsante "Copia Codice"
- [ ] Controlla la lista partecipanti (dovresti essere il primo)

### 4.2 Informazioni Torneo
- [ ] Verifica che tutte le info siano corrette:
  - [ ] Nome torneo
  - [ ] Lega selezionata  
  - [ ] Preset scelto
  - [ ] Numero massimo giocatori
  - [ ] Data di inizio

---

## 👥 **FASE 5: Test Join Torneo (Seconda Finestra)**

### 5.1 Preparazione
- [ ] Apri una **nuova finestra in incognito** o un **altro browser**
- [ ] Vai a https://fantamatch.netlify.app
- [ ] NON fare login (testa come visitatore)

### 5.2 Join tramite Codice
- [ ] Vai all'URL: `https://fantamatch.netlify.app/join/[IL-TUO-CODICE]`
  - Sostituisci `[IL-TUO-CODICE]` con il codice copiato prima
- [ ] Dovrebbe apparire la pagina di anteprima torneo
- [ ] Verifica che vedi le informazioni corrette
- [ ] Inserisci un **Nome Display**: "Giocatore Test"
- [ ] Clicca "Unisciti al Torneo"

### 5.3 Verifica Join
- [ ] Dovrebbe apparire conferma di partecipazione
- [ ] Torna alla finestra originale (dove sei loggato)
- [ ] Ricarica la pagina del torneo
- [ ] Verifica che "Giocatore Test" appaia nella lista partecipanti

---

## 🔄 **FASE 6: Test Funzionalità Multi-Torneo**

### 6.1 Crea Secondo Torneo
- [ ] Dalla tua finestra principale, crea un altro torneo:
  - Nome: "Premier League Test"
  - Lega: Premier League
  - Preset diverso dal primo
- [ ] Verifica che entrambi i tornei appaiano nella dashboard

### 6.2 Test Dashboard Tornei
- [ ] Vai alla Dashboard principale
- [ ] Verifica che la sezione "Tornei" mostri:
  - [ ] Entrambi i tuoi tornei
  - [ ] Stato corretto (es. "In Attesa")
  - [ ] Numero partecipanti aggiornato

---

## 📱 **FASE 7: Test Responsivo**

### 7.1 Mobile Testing
- [ ] Prova tutto il sito su mobile (o modalità sviluppatore)
- [ ] Verifica che la sidebar diventi un hamburger menu
- [ ] Testa la creazione torneo su mobile
- [ ] Verifica che il join torneo funzioni su mobile
- [ ] Controlla che tutti i testi siano leggibili

### 7.2 Tablet Testing  
- [ ] Testa su tablet o schermo medio
- [ ] Verifica layout a 2 colonne dove appropriato

---

## 🔍 **FASE 8: Test Scenario Completi**

### 8.1 Scenario Completo - Torneo Pieno
- [ ] Crea un torneo con max 3 giocatori
- [ ] Fai join con 2 browser diversi (2 partecipanti extra)
- [ ] Prova a far join un 4° giocatore
- [ ] Verifica che mostri "Torneo Pieno"

### 8.2 Test Codici Invito
- [ ] Prova a visitare `/join/CODICE-INESISTENTE`
- [ ] Verifica che mostri errore appropriato
- [ ] Prova con codici malformati
- [ ] Verifica gestione errori

### 8.3 Test Persistenza Dati
- [ ] Crea tornei e partecipa
- [ ] Ricarica la pagina
- [ ] Verifica che tutto persista (localStorage)
- [ ] Chiudi e riapri browser
- [ ] Controlla che i dati ci siano ancora

---

## 🐛 **COSA ANNOTARE DURANTE I TEST**

### ✅ Funzionalità che Funzionano Bene
- Elenca cosa funziona perfettamente

### ❌ Problemi Trovati
Per ogni problema, annota:
- **Dove**: Quale pagina/sezione
- **Cosa**: Cosa hai fatto
- **Risultato**: Cosa è successo
- **Atteso**: Cosa ti aspettavi
- **Browser**: Chrome/Safari/Firefox
- **Dispositivo**: Desktop/Mobile/Tablet

### 💡 Suggerimenti UX
- Design che potrebbe essere migliorato
- Testo poco chiaro
- Funzionalità che sembrano mancare
- Idee per miglioramenti

---

## 🎯 **CHECKLIST FINALE**

- [ ] Login funziona
- [ ] Dashboard si carica correttamente  
- [ ] Creazione torneo completa
- [ ] Join torneo funziona
- [ ] Multi-browser testing completato
- [ ] Mobile responsive testato
- [ ] Tutti i testi in italiano sono corretti
- [ ] Cambio lingua funziona
- [ ] Persistenza dati verificata
- [ ] Gestione errori testata

---

## 📝 **COME CONDIVIDERE I RISULTATI**

Crea un documento con:

1. **Sezione FUNZIONA**: Cosa va bene
2. **Sezione PROBLEMI**: Lista dettagliata bug
3. **Sezione SUGGERIMENTI**: Idee miglioramento
4. **SCREENSHOT**: Se possibile, aggiungi screenshot dei problemi

**Grazie per i test approfonditi! 🚀**

---

## 🔧 **INFO TECNICHE (Se Serve)**

- **Build**: Versione di sviluppo
- **Tecnologie**: Next.js, React, TypeScript
- **Storage**: localStorage (temporaneo)
- **API**: Mock data per ora
- **Target**: Chrome/Safari/Firefox moderni

Qualsiasi domanda, chiedi pure! 🇮🇹