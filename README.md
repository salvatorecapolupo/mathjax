# Editor LaTeX in HTML

**Cos'è:**
È un'applicazione web contenuta in un singolo file HTML (senza bisogno di server) che funge da *sandbox* per scrivere e visualizzare formule matematiche in tempo reale usando la sintassi LaTeX per il web.

**Come funziona:**

1. **Motore di Rendering (MathJax 3):** Il codice carica **MathJax** da una fonte sicura (JSDelivr). Questa libreria legge il testo delimitato da `$$` (formule a blocco) o `$` (formule in linea) e lo trasforma istantaneamente in grafica vettoriale nitida.
2. **Interattività (JavaScript):** Uno script ascolta ogni tasto che premi nella casella di testo (`input event`). Appena modifichi il testo, lancia una "Promise" che chiede a MathJax di riprocessare (`typeset`) l'area di anteprima.
3. **Sicurezza:** Il codice è stato ripulito da dipendenze obsolete e pericolose (come *polyfill.io*), utilizzando solo standard moderni supportati dai browser attuali.

**A cosa serve:**
È uno strumento pronto all'uso per imparare la sintassi, testare equazioni complesse (come sistemi o frazioni annidate) e copiare il codice funzionante nei propri progetti scolastici o documenti web.
