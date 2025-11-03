
# Ghid de Configurare Ollama

Acest proiect a fost actualizat pentru a folosi **Ollama** în loc de OpenAI/ChatGPT. Ollama permite rularea modelelor de limbaj local pe propriul tău calculator.

## Instalare Ollama

### macOS
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

Sau descarcă direct de pe [ollama.com](https://ollama.com)

### Linux
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### Windows
Descarcă installerul de pe [ollama.com](https://ollama.com)

## Descărcarea Modelului

După instalarea Ollama, trebuie să descarci un model. Codul folosește implicit `gemma3:270m`:

```bash
ollama pull gemma3:270m
```

### Modele Alternative Recomandate

- **gemma3:270m** (implicit) - Balansat, performanță bună
- **gemma3:270m:1b** - Mai mic și mai rapid
- **mistral** - Alternative excelent la llama
- **phi3** - Model mic dar performant

Pentru a folosi un alt model:
```bash
ollama pull mistral
```

## Pornirea Serverului Ollama

Ollama rulează ca un server local pe portul 11434. După instalare, serverul ar trebui să pornească automat.

Pentru a verifica dacă serverul rulează:
```bash
curl http://localhost:11434/api/version
```

Pentru a porni manual serverul (dacă este necesar):
```bash
ollama serve
```

## Instalarea Dependențelor Python

```bash
pip install -r requirements.txt
```

## Rularea Exemplelor

### 1. Intelligence (Inteligență de bază)
```bash
python 1-intelligence.py
```

### 2. Memory (Memorie conversațională)
```bash
python 2-memory.py
```

### 3. Tools (Integrare cu instrumente externe)
```bash
python 3-tools.py
```

### 4. Validation (Validare schema structurată)
```bash
python 4-validation.py
```

### 5. Control (Control flux deterministic)
```bash
python 5-control.py
```

### 6. Recovery (Gestionare erori și retry)
```bash
python 6-recovery.py
```

### 7. Feedback (Aprobare umană)
```bash
python 7-feedback.py
```

## Schimbarea Modelului

Toate funcțiile acceptă un parametru `model` pentru a schimba modelul folosit:

```python
from intelligence import basic_intelligence

# Folosește modelul implicit (gemma3:270m)
result = basic_intelligence("What is AI?")

# Folosește un alt model
result = basic_intelligence("What is AI?", model="mistral")
```

## Depanare

### Eroare: Connection refused
Asigură-te că serverul Ollama rulează:
```bash
ollama serve
```

### Eroare: Model not found
Descarcă modelul mai întâi:
```bash
ollama pull gemma3:270m
```

### Performanță lentă
- Folosește un model mai mic: `gemma3:270m:1b`
- Verifică resursele sistemului (RAM, CPU)
- Consideră folosirea GPU dacă este disponibil

## Diferențe față de OpenAI

1. **Rulare locală**: Totul rulează pe computerul tău, fără costuri API
2. **Confidențialitate**: Datele tale rămân local
3. **Personalizare**: Poți folosi diverse modele open-source
4. **Performanță**: Depinde de hardware-ul tău

## Resurse Suplimentare

- [Documentație Ollama](https://github.com/ollama/ollama)
- [API Reference](https://github.com/ollama/ollama/blob/main/docs/api.md)
- [Modele Disponibile](https://ollama.com/library)

