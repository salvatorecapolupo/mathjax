# Editor LaTeX in HTML

**A cosa serve**
È un'applicazione web contenuta in un singolo file HTML (senza bisogno di server) che funge da *sandbox* per scrivere e visualizzare formule matematiche in tempo reale usando la sintassi LaTeX per il web.

**Come funziona:**

1. **Motore di Rendering (MathJax 3):** Il codice carica **MathJax** da una fonte sicura (JSDelivr). Questa libreria legge il testo delimitato da `$$` (formule a blocco) o `$` (formule in linea) e lo trasforma istantaneamente in grafica vettoriale nitida.
2. **Interattività (JavaScript):** Uno script ascolta ogni tasto che premi nella casella di testo (`input event`). Appena modifichi il testo, lancia una "Promise" che chiede a MathJax di riprocessare (`typeset`) l'area di anteprima.
3. Versione alpha. 

**Nella didattica**
È uno strumento pronto all'uso per imparare la sintassi, testare equazioni complesse (come sistemi o frazioni annidate) e copiare il codice funzionante nei propri progetti scolastici o documenti web.

Ecco la spiegazione delle differenze principali:

# Editor LaTeX (MathJax) vs MathJS

La differenza fondamentale risiede nello scopo: uno serve per **scrivere** (forma), l'altro per **calcolare** (contenuto).

### 1. Il Software Fornito (MathJax)

* **Ruolo:** È un motore di **Rendering** (visualizzazione).
* **Cosa fa:** Traduce un codice testuale (es. `\frac{1}{2}`) in una grafica vettoriale bella da vedere.
* **Logica:** Non "capisce" la matematica. Se scrivi `$$2 + 2 = 5$$`, il software lo visualizzerà perfettamente senza segnalare errori, perché la sintassi LaTeX è corretta, anche se la matematica è sbagliata.
* **Analogia:** È come **Microsoft Word** o una macchina da scrivere elegante.

### 2. MathJS

* **Ruolo:** È un motore di **Calcolo** (Computer Algebra System).
* **Cosa fa:** Analizza l'espressione matematica per risolverla, semplificarla o valutarla numericamente.
* **Logica:** Capisce le regole matematiche. Se gli dai in pasto `2 + 2`, ti restituisce `4`. Se gli chiedi la derivata di , calcola .
* **Analogia:** È come una **Calcolatrice Scientifica** o Excel.

### Tabella Riassuntiva

| Caratteristica | Editor LaTeX (MathJax) | MathJS |
| --- | --- | --- |
| **Obiettivo** | Tipografia e pubblicazione | Risoluzione e calcolo |
| **Input** | Codice di markup (`\sqrt{x}`) | Espressioni logiche (`sqrt(x)`) |
| **Output** | Immagine/Grafica della formula | Risultato numerico o simbolico |
| **Errore se:** | Sbagli le parentesi del codice | Dividi per zero o sintassi invalida |

**In sintesi:** Usi il codice che ti ho dato per **mostrare** i compiti a casa sul web; useresti MathJS per **farli** risolvere al computer.
