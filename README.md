# Projekt Rotory

## Opis projektu

Projekt analizuje dane wiatrowe i falowe w celu budowania modelu predykcyjnego dla rotorów.

---

## Jak uruchomić notebook

### Wymagania wstępne

- Python 3.8+
- pip
- virtualenv (opcjonalnie, ale zalecane)

### Kroki uruchomienia

1. **Klonuj repozytorium i przejdź do folderu projektu**

   ```bash
   cd projekt-rotory
   ```

2. **Utwórz wirtualne środowisko (opcjonalne, ale zalecane)**

   ```bash
   python -m venv venv
   ```

3. **Aktywuj wirtualne środowisko**

   **Na Windows (PowerShell):**

   ```powershell
   .\venv\Scripts\Activate.ps1
   ```

   **Na Windows (Command Prompt):**

   ```cmd
   venv\Scripts\activate.bat
   ```

   **Na macOS/Linux:**

   ```bash
   source venv/bin/activate
   ```

4. **Zainstaluj wymagane biblioteki**

   ```bash
   pip install -r requirements.txt
   ```

5. **Uruchom Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

6. **Otwórz notebook**
   - W przeglądarce internetowej otwórz interfejs Jupyter
   - Kliknij na plik `01_czyszczenie_danych-2-2.ipynb`
   - Wykonaj komórki w kolejności (Shift + Enter lub przycisk "Run")

### Alternatywnie - Uruchomienie z VS Code

1. Otwórz VS Code w folderze projektu
2. Zainstaluj rozszerzenie "Jupyter" dla VS Code
3. Otwórz plik `01_czyszczenie_danych-2-2.ipynb`
4. Wybierz wirtualne środowisko jako kernel
5. Uruchamiaj komórki klikając na przycisk "Run Cell"

---

## Struktura projektu

```
projekt-rotory/
├── 01_czyszczenie_danych-2-2.ipynb   # Główny notebook z analizą
├── requirements.txt                   # Wymagane biblioteki
├── xgboost_model_rotory.joblib       # Wytrenowany model XGBoost
├── xgboost_lista_cech.joblib         # Lista cech modelu
├── dane_gotowe_rotor.csv             # Przetworzone dane
├── raport.csv                        # Raport z wynikami
└── Dane/                             # Folder z danymi wejściowymi
    ├── *.nc                          # Pliki NetCDF z danymi
    ├── currents/                     # Dane o prądach oceanicznych
    └── sea_level/                    # Dane o poziomie morza
```

---

## Wymagane biblioteki

Główne biblioteki używane w projekcie:

- `xarray` - praca z danymi NetCDF
- `netCDF4` - obsługa formatów NetCDF
- `pandas` - analiza danych
- `xgboost` - modele uczenia maszynowego
- `scikit-learn` - narzędzia ML
- `jupyter` - interaktywne notebooki

Pełna lista znajduje się w pliku `requirements.txt`.

---

## Notki

- Notebook oczekuje danych w folderze `Dane/`
- Wyniki są zapisywane w plikach CSV
- Model XGBoost jest załadowany z pliku `.joblib`
