# Maturitní okruhy SWA (Informační technologie) 🎓

Moderní, interaktivní a responzivní webová aplikace sloužící jako prémiová studijní pomůcka pro přípravu na prezenční maturitní zkoušku z oboru Informační Technologie. Aplikace obsahuje 15 plně vypracovaných osnov (otázky 12 až 26) rozdělených na Teoretickou a Praktickou část.

## ✨ Klíčové Vlastnosti
- **Kompletní obsah:** Vypracovaných 15 maturitních témat (Hardware, Sítě, Bezpečnost, MS Office, DB, Web, Projektové řízení).
- **Prémiový Design:** Tmavé téma využívající *Glassmorphism* styl (rozostřené karty), plynulé animace a živé pulzující mesh-gradientní pozadí.
- **Interaktivní ukázky:** Záložky pro praktické příklady (simulace Kanban nástěnky, funkční Fetch API na kliknutí tlačítka).
- **Detached Layout:** Plovoucí "Dashboard" boční navigační panel s lepším využitím prostoru.

## 🛠️ Technologie
Projekt byl od základu přepsán ze starého statického HTML na moderní frontendový stack (SPA):
* **[Vue 3](https://vuejs.org/)** (Composition API)
* **[Vite](https://vitejs.dev/)** (Lightning fast formátování)
* **Custom Vanilla CSS** (CSS Proměnné pro absolutní kontrolu layoutu a stínů)
* **Chart.js** (Pro dynamické HTML plátno - `canvas`)

## 🚀 Jak spustit projekt lokálně

Před spuštěním samotného kódu se ujistěte, že máte v počítači nainstalovaný [Node.js](https://nodejs.org/).

1. **Klonování repozitáře**
```bash
git clone https://github.com/Jag3r20/maturitni_okruhy_swa.git
cd maturitni_okruhy_swa
```

2. **Instalace závislostí**
```bash
npm install
```

3. **Spuštění vývojového serveru**
```bash
npm run dev
```

Po úspěšném sestavení bude aplikace dostupná ve vašem prohlížeči na adrese: `http://localhost:5173`. 

---
Vygenerováno za účelem výuky a usnadnění studia SWA ✨
