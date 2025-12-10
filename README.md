# PasswordGenerator

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)

PasswordGenerator è un progetto in **C++** per generare password sicure e configurabili.  
È pensato per imparare **CMake**, migliorare le competenze in **C++** e fare pratica con **Git**.

---

## 🔹 Funzionalità principali

- Generazione di password casuali e sicure
- Configurazione di lunghezza, simboli, maiuscole/minuscole
- Possibilità di generare più password contemporaneamente
- Interfaccia CLI semplice e leggibile
- Struttura modulare: libreria (`passwordgen_lib`) + CLI (`passwordgen_cli`)

---

## 📂 Struttura del progetto

PasswordGenerator/
├─ include/PasswordGenerator/
│ ├─ Generator.h
│ └─ Config.h
├─ src/
│ ├─ Generator.cpp
│ └─ Config.cpp
├─ app/
│ └─ main.cpp
├─ tests/
│ └─ test_main.cpp
├─ CMakeLists.txt
└─ README.md


---

## ⚙️ Roadmap di sviluppo

### Fase 1 — Strutturazione Base
- Libreria (`passwordgen_lib`) + eseguibile (`passwordgen_cli`)
- CMake moderno con target e include directories

### Fase 2 — API e Modello di Generazione
- Classe `PasswordGenerator`
- Configurazioni: lunghezza, simboli, maiuscole/minuscole
- Gestione errori e input invalidi

### Fase 3 — Migliorie CMake
- Opzioni `ENABLE_SYMBOLS`, `DEFAULT_LENGTH`
- Build Debug/Release con flag dedicati
- Target moderni e pulizia generale

### Fase 4 — Testing
- GoogleTest / Catch2 integrato con `FetchContent`
- Test unitari su lunghezza, caratteri e configurazioni
- Esecuzione test con `ctest`

### Fase 5 — CLI Evoluta
- Parser dei parametri (CLI11 o cxxopts)
- Opzioni CLI:
  - `--length <num>`
  - `--symbols`
  - `--count <num>`
  - `--no-lowercase`
- Output leggibile e formattato

### Fase 6 — Miglioramento Architetturale
- Strategy Pattern per più generatori
- File di configurazione (JSON/TOML)
- Modulo di valutazione forza (entropia + blacklist parole comuni)

### Fase 7 — Installazione & Packaging
- Target `install` in CMake
- Distribuzione headers, libreria e CLI
- CPack per pacchetti `.deb`, `.rpm`, `.zip`

### Fase 8 — Continuous Integration (CI)
- GitHub Actions per build multi-OS
- Test automatici e badge di stato nel README

### Fase 9 — Documentazione
- Doxygen per documentazione API
- README aggiornato con esempi
- CHANGELOG e versioning semantico

### Fase 10 — GUI (Opzionale)
- GUI minima con Qt / ImGui / GTK
- Slider e checkbox per configurazioni
- Pulsante “Generate” con copy-to-clipboard

---

## 🛠️ Compilazione e installazione

```bash
git clone git@github.com:USERNAME/PasswordGenerator.git
cd PasswordGenerator
mkdir build && cd build
cmake ..
cmake --build .
sudo cmake --install .
```