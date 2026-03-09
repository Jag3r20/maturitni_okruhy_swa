<script setup>
import { onMounted, ref } from 'vue'
import Chart from 'chart.js/auto'

const phasesChartRef = ref(null)

onMounted(() => {
  if (phasesChartRef.value) {
    new Chart(phasesChartRef.value, {
      type: 'bar',
      data: {
        labels: ['Fáze 1 (Konceptualní)', 'Fáze 2 (Logická)', 'Fáze 3 (Fyzická)'],
        datasets: [{
          label: 'Fáze návrhu (Zjednodušená zátěž/důležitost)',
          data: [1, 2, 3],
          backgroundColor: ['#3b82f6', '#0ea5e9', '#8b5cf6'],
          borderRadius: 6
        }]
      },
      options: {
        responsive: true,
        plugins: {
          legend: { display: false }
        },
        scales: { 
          y: { 
            beginAtZero: true,
            ticks: { color: '#94a3b8' },
            grid: { color: 'rgba(255,255,255,0.05)' }
          },
          x: {
            ticks: { color: '#94a3b8' },
            grid: { display: false }
          }
        }
      }
    });
  }
})
</script>

<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Úvod</h2>
      <p>Návrh databáze je klíčovou fází vývoje softwaru. <strong>Špatně navržená databáze</strong> vede k redundanci (opakování) dat, nekonzistenci (různé údaje o téže věci na různých místech) a pomalému výkonu. Cílem návrhu je vytvořit strukturu, která efektivně ukládá data a zachovává jejich integritu.</p>
      
      <div class="steps-horizontal">
        <div class="step-box">
          <div class="step-num">1</div>
          <div class="step-text">Konceptuální návrh (ER diagramy)</div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box">
          <div class="step-num">2</div>
          <div class="step-text">Logický návrh (Normalizace)</div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box">
          <div class="step-num">3</div>
          <div class="step-text">Fyzický návrh (SQL kód)</div>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Praktická ukázka: Databáze pro E-shop</h2>
      <p>Pro demonstraci budeme navrhovat zjednodušený systém pro e-shop.</p>
      <div class="info-box accent">
        <p><strong>Zadání:</strong> Potřebujeme evidovat zákazníky, produkty a objednávky. Víme, že jedna objednávka může obsahovat více produktů a jeden produkt může být ve více objednávkách.</p>
      </div>
      <div class="image-wrapper">
        <img src="https://svg.template.creately.com/drem47fZBw8" alt="ER diagram for online shopping system" style="background:#fff">
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Fáze 1: Konceptuální model (ER Diagram)</h2>
      <p>V této fázi nás nezajímají tabulky ani datové typy, ale entity (objekty) a vztahy mezi nimi.</p>
      
      <div class="grid-2-col">
        <div>
          <h3>Identifikované entity:</h3>
          <ul class="styled-list">
            <li><strong>Zákazník</strong> (Jméno, Email, Adresa)</li>
            <li><strong>Produkt</strong> (Název, Cena)</li>
            <li><strong>Objednávka</strong> (Datum, Stav)</li>
          </ul>
        </div>
        
        <div>
          <h3>Vztahy:</h3>
          <ul class="styled-list number-icons">
            <li>Zákazník vytváří Objednávku <em>(Vztah 1:N – 1 zákazník má mnoho objednávek)</em>.</li>
            <li>Objednávka obsahuje Produkty <em>(Vztah M:N – mnoho produktů v mnoha objednávkách)</em>.</li>
          </ul>
        </div>
      </div>
      
      <div class="notice border-left">
        <strong>Poznámka:</strong> Vztah M:N (Mnoho k mnoha) je v relačních databázích problematický a v další fázi jej budeme muset rozbít pomocí tzv. vazební tabulky.
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Fáze 2: Logický návrh a Normalizace</h2>
      <p>Představme si, že bychom vše nacpali do jedné tabulky. To by byla chyba:</p>
      
      <div class="table-container bad-table">
        <table>
          <thead>
            <tr>
              <th>ID_Obj</th>
              <th>Zákazník</th>
              <th>Adresa</th>
              <th>Produkt</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>101</td>
              <td class="highlight-error">Jan Novák</td>
              <td class="highlight-error">Praha 1</td>
              <td>Notebook</td>
            </tr>
            <tr>
              <td>102</td>
              <td class="highlight-error">Jan Novák</td>
              <td class="highlight-error">Praha 1</td>
              <td>Myš</td>
            </tr>
          </tbody>
        </table>
        <div class="table-caption error-text">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" class="icon" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"></circle><line x1="15" y1="9" x2="9" y2="15"></line><line x1="9" y1="9" x2="15" y2="15"></line></svg>
          Problém: Redundance dat. Jméno a adresa se zbytečně opakují.
        </div>
      </div>

      <h3>Řešení (Rozdělení do tabulek 3NF):</h3>
      <div class="card-grid">
        <div class="schema-card">
          <div class="schema-title">Zakaznici</div>
          <div class="schema-fields">zakaznik_id (PK), jmeno, email...</div>
        </div>
        <div class="schema-card">
          <div class="schema-title">Produkty</div>
          <div class="schema-fields">produkt_id (PK), nazev, cena</div>
        </div>
        <div class="schema-card">
          <div class="schema-title">Objednavky</div>
          <div class="schema-fields">objednavka_id (PK), zakaznik_id (FK), datum</div>
        </div>
        <div class="schema-card highlight">
          <div class="schema-title">Polozky_Objednavky <span class="badge">Vazební</span></div>
          <div class="schema-fields">id (PK), objednavka_id (FK), produkt_id (FK), pocet</div>
        </div>
      </div>
      
      <div class="image-wrapper compact">
        <img src="https://cdn.hackr.io/uploads/posts/attachments/1666888816mdnYlrMoEE.png" alt="Normalization in DBMS">
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Fáze 3: Fyzický návrh (SQL Kód)</h2>
      <p>Toto je finální kód, který spustíme v databázi (např. MySQL). Zde definujeme datové typy a klíče.</p>
      
      <div class="sql-terminal">
        <div class="sql-header">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
          <span class="title">eshop_schema.sql</span>
        </div>
<pre><code><span class="comment">-- 1. Tabulka Zákazníků</span>
<span class="keyword">CREATE TABLE</span> <span class="table">Zakaznici</span> (
    <span class="column">zakaznik_id</span> INT <span class="keyword">PRIMARY KEY AUTO_INCREMENT</span>,
    <span class="column">jmeno</span> VARCHAR(100) <span class="keyword">NOT NULL</span>,
    <span class="column">email</span> VARCHAR(100) <span class="keyword">UNIQUE NOT NULL</span>,
    <span class="column">adresa</span> VARCHAR(255)
);

<span class="comment">-- 2. Tabulka Produktů</span>
<span class="keyword">CREATE TABLE</span> <span class="table">Produkty</span> (
    <span class="column">produkt_id</span> INT <span class="keyword">PRIMARY KEY AUTO_INCREMENT</span>,
    <span class="column">nazev</span> VARCHAR(100) <span class="keyword">NOT NULL</span>,
    <span class="column">cena</span> DECIMAL(10, 2) <span class="keyword">NOT NULL</span>
);

<span class="comment">-- 3. Tabulka Objednávek</span>
<span class="keyword">CREATE TABLE</span> <span class="table">Objednavky</span> (
    <span class="column">objednavka_id</span> INT <span class="keyword">PRIMARY KEY AUTO_INCREMENT</span>,
    <span class="column">zakaznik_id</span> INT, <span class="comment">-- Cizí klíč</span>
    <span class="column">datum_vytvoreni</span> DATETIME <span class="keyword">DEFAULT CURRENT_TIMESTAMP</span>,
    <span class="keyword">FOREIGN KEY</span> (zakaznik_id) <span class="keyword">REFERENCES</span> <span class="table">Zakaznici</span>(zakaznik_id)
);

<span class="comment">-- 4. Vazební tabulka (řeší vztah M:N)</span>
<span class="keyword">CREATE TABLE</span> <span class="table">Polozky_Objednavky</span> (
    <span class="column">id</span> INT <span class="keyword">PRIMARY KEY AUTO_INCREMENT</span>,
    <span class="column">objednavka_id</span> INT,
    <span class="column">produkt_id</span> INT,
    <span class="column">pocet_kusu</span> INT <span class="keyword">DEFAULT</span> 1,
    <span class="keyword">FOREIGN KEY</span> (objednavka_id) <span class="keyword">REFERENCES</span> <span class="table">Objednavky</span>(objednavka_id),
    <span class="keyword">FOREIGN KEY</span> (produkt_id) <span class="keyword">REFERENCES</span> <span class="table">Produkty</span>(produkt_id)
);</code></pre>
      </div>
      
      <p class="mt-4">
        <strong>Vysvětlení:</strong> V tabulce <code>Objednavky</code> neukládáme jméno zákazníka, ale pouze <code>zakaznik_id</code>. Pokud se Jan Novák přejmenuje, změníme to jen v tabulce <code>Zakaznici</code> a všechny jeho objednávky zůstanou platné. To je síla relační databáze.
      </p>
    </section>

    <section class="glass-panel content-section">
      <h2>Závěr</h2>
      <p>Kvalitní návrh databáze připomíná stavbu domu.</p>
      
      <div class="grid-2-col align-start">
        <ul class="styled-list custom-bullets">
          <li><strong>1. Nákres:</strong> ER Diagram (Máme jasný plán)</li>
          <li><strong>2. Rozvržení:</strong> Normalizace (Žádné zbytečné místnosti a nepořádek)</li>
          <li><strong>3. Stavba:</strong> SQL kód (Cihla k cihle)</li>
        </ul>
        
        <div class="chart-container mini">
          <canvas ref="phasesChartRef"></canvas>
        </div>
      </div>
      
      <div class="success-box">
        Dodržení tohoto postupu zajišťuje, že aplikace bude stabilní, data budou v bezpečí a systém bude možné v budoucnu snadno rozšiřovat.
      </div>
    </section>
  </div>
</template>

<style scoped>
.topic-content-wrapper {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  padding-bottom: 4rem;
}

.content-section {
  padding: 2rem;
  transition: transform var(--transition-base), box-shadow var(--transition-base);
}

.content-section:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
  border-color: rgba(59, 130, 246, 0.3);
}

.content-section h2 {
  color: var(--color-primary);
  margin-top: 0;
}

.mt-4 {
  margin-top: 1.5rem;
}

h3 {
  color: #fff;
}

/* Horizontal Steps Flow */
.steps-horizontal {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 2rem 0;
  flex-wrap: wrap;
  gap: 1rem;
}

@media (max-width: 768px) {
  .steps-horizontal {
    flex-direction: column;
    align-items: stretch;
  }
  .step-arrow {
    transform: rotate(90deg);
    text-align: center;
    margin: 0.5rem 0;
  }
}

.step-box {
  flex: 1;
  background: rgba(30, 41, 59, 0.5);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-md);
  padding: 1rem;
  display: flex;
  align-items: center;
  gap: 1rem;
  min-width: 200px;
}

.step-num {
  background: var(--color-primary);
  color: white;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

.step-text {
  font-weight: 500;
  color: #e2e8f0;
}

.step-arrow {
  color: var(--color-text-muted);
  font-size: 1.5rem;
  font-weight: 300;
}

.info-box {
  background: rgba(59, 130, 246, 0.1);
  border-left: 4px solid var(--color-primary);
  padding: 1.5rem;
  border-radius: 0 var(--radius-md) var(--radius-md) 0;
  margin: 1.5rem 0;
}

.info-box.accent {
  background: rgba(139, 92, 246, 0.1);
  border-color: var(--color-accent);
}

.info-box p:last-child {
  margin-bottom: 0;
}

.success-box {
  background: rgba(16, 185, 129, 0.1);
  border-left: 4px solid #10b981;
  padding: 1rem 1.5rem;
  border-radius: var(--radius-md);
  margin-top: 1.5rem;
  color: #d1fae5;
}

/* Images */
.image-wrapper {
  margin: 1.5rem 0;
  border-radius: var(--radius-md);
  overflow: hidden;
  box-shadow: var(--shadow-md);
  border: 1px solid var(--color-border);
  background: #fff; /* For diagrams that are not transparent */
}

.image-wrapper.compact {
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.image-wrapper img {
  display: block;
  width: 100%;
  height: auto;
  transition: transform 0.5s ease;
}

.image-wrapper:hover img {
  transform: scale(1.02);
}

/* Data Tables */
.table-container {
  overflow-x: auto;
  margin: 1.5rem 0;
  background: rgba(15, 23, 42, 0.8);
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border);
}

.table-container table {
  width: 100%;
  border-collapse: collapse;
}

.table-container th, .table-container td {
  padding: 0.75rem 1rem;
  text-align: left;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.table-container th {
  background: rgba(0, 0, 0, 0.3);
  color: var(--color-primary-hover);
  font-weight: 600;
}

.highlight-error {
  background: rgba(239, 68, 68, 0.2);
  color: #fca5a5;
}

.table-caption {
  padding: 0.75rem 1rem;
  font-size: 0.875rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  background: rgba(0, 0, 0, 0.2);
}

.error-text {
  color: #f87171;
}

.icon {
  flex-shrink: 0;
}

/* Schema Cards Layout */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  margin: 1.5rem 0;
}

.schema-card {
  background: rgba(30, 41, 59, 0.6);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-md);
  overflow: hidden;
}

.schema-card.highlight {
  border-color: rgba(139, 92, 246, 0.5);
  box-shadow: 0 4px 12px rgba(139, 92, 246, 0.15);
}

.schema-title {
  background: rgba(0, 0, 0, 0.4);
  padding: 0.75rem 1rem;
  font-weight: 600;
  border-bottom: 1px solid var(--color-border);
  color: var(--color-primary-hover);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.badge {
  font-size: 0.7rem;
  background: var(--color-accent);
  color: white;
  padding: 2px 6px;
  border-radius: 4px;
}

.schema-fields {
  padding: 1rem;
  font-size: 0.85rem;
  color: #cbd5e1;
  font-family: monospace;
}

/* Standard UI utilities */
.grid-2-col {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  align-items: center;
}

.align-start {
  align-items: flex-start;
}

@media (max-width: 768px) {
  .grid-2-col { grid-template-columns: 1fr; }
}

.styled-list {
  list-style: none;
  padding: 0;
}

.styled-list li {
  position: relative;
  padding-left: 1.5rem;
  margin-bottom: 0.75rem;
}

.styled-list li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: var(--color-primary);
  font-weight: bold;
}

.styled-list.custom-bullets li::before {
  content: '✓';
  color: #10b981;
}

.notice.border-left {
  border: none;
  border-left: 4px solid var(--color-accent);
  background: rgba(15, 23, 42, 0.5);
  border-radius: 0 var(--radius-md) var(--radius-md) 0;
}

/* SQL Code Block Editor look */
.sql-terminal {
  background: #0d1117;
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border);
  overflow: hidden;
  margin: 1.5rem 0;
}

.sql-header {
  background: #161b22;
  padding: 0.5rem 1rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.dot.red { background: #ff5f56; }
.dot.yellow { background: #ffbd2e; }
.dot.green { background: #27c93f; }

.sql-header .title {
  margin-left: 1rem;
  font-family: monospace;
  font-size: 0.85rem;
  color: #8b949e;
}

.sql-terminal pre {
  margin: 0;
  background: transparent;
  border: none;
  border-radius: 0;
}

/* SQL syntax styling simulation */
.sql-terminal .comment { color: #8b949e; font-style: italic; }
.sql-terminal .keyword { color: #ff7b72; font-weight: bold; }
.sql-terminal .table { color: #79c0ff; }
.sql-terminal .column { color: #d2a8ff; }

/* Chart wrapper */
.chart-container.mini {
  background: rgba(15, 23, 42, 0.4);
  padding: 1rem;
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border);
  height: 200px;
  width: 100%;
}
</style>
