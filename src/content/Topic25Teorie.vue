<script setup>
import { onMounted, ref } from 'vue'
import Chart from 'chart.js/auto'

const databaseChartRef = ref(null)

onMounted(() => {
  if (databaseChartRef.value) {
    new Chart(databaseChartRef.value, {
      type: 'doughnut',
      data: {
        labels: ['Data', 'Aplikace', 'Databáze', 'DBMS'],
        datasets: [{
          label: 'Databázový systém',
          data: [25, 25, 25, 25],
          backgroundColor: ['#3b82f6', '#0ea5e9', '#8b5cf6', '#1e293b'],
          borderWidth: 0,
          hoverOffset: 4
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: { 
            position: 'right',
            labels: { color: '#f8fafc' }
          }
        }
      }
    })
  }
})
</script>

<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Úvod do světa databází</h2>
      <p>V dnešní digitální éře jsou data cenným aktivem. <strong>Správný návrh databáze</strong> je zásadní pro jejich efektivní ukládání, vyhledávání a manipulaci. Bez dobře strukturované databáze se i ty nejlepší aplikace potýkají s problémy s výkonem a integritou dat.</p>
      
      <div class="info-box">
        <p><em>Proč je návrh databáze důležitý?</em> Zajišťuje integritu, konzistenci a bezpečnost dat.</p>
        <p><strong>Co je cílem?</strong> Vytvořit robustní, škálovatelný a snadno udržovatelný datový systém.</p>
        <p><strong>Kdo to potřebuje?</strong> Každá aplikace, od malého webu po rozsáhlý podnikový systém.</p>
      </div>
      
      <div class="image-wrapper">
        <img src="https://miro.medium.com/v2/resize:fit:1400/1*kv-24zUQuUmC4vxIMlzILw.jpeg" alt="Relational database design illustration">
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Teoretické základy: Co je databáze?</h2>
      <p>Databáze je organizovaná kolekce strukturovaných informací neboli dat, typicky uložených elektronicky v počítačovém systému. Databázový systém se obvykle skládá z databázového stroje (DBMS), který umožňuje uživatelům spravovat a interagovat s daty.</p>
      
      <div class="grid-2-col">
        <ul class="styled-list">
          <li><strong>Data:</strong> Neorganizované informace.</li>
          <li><strong>Aplikace:</strong> Rozhraní pro uživatele.</li>
          <li><strong>Databáze:</strong> Organizovaná kolekce dat.</li>
          <li><strong>DBMS:</strong> Software pro správu databází (např. MySQL, PostgreSQL).</li>
        </ul>
        <div class="chart-container">
          <canvas ref="databaseChartRef"></canvas>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Relační databáze a SQL</h2>
      <p>Relační databáze ukládají data v tabulkách, které jsou vzájemně propojeny pomocí klíčů. Jsou základem mnoha systémů díky své strukturovanosti a schopnosti udržovat integritu dat.</p>
      
      <div class="two-columns-layout">
        <div>
          <h3>Klíčové pojmy</h3>
          <ul class="styled-list">
            <li><strong>Tabulka (Table):</strong> Skládá se z řádků a sloupců.</li>
            <li><strong>Řádek (Row/Record):</strong> Jedna položka v tabulce.</li>
            <li><strong>Sloupec (Column/Field):</strong> Atribut (vlastnost) záznamu.</li>
            <li><strong>Primární klíč (Primary Key):</strong> Unikátní identifikátor řádku.</li>
            <li><strong>Cizí klíč (Foreign Key):</strong> Odkazuje na primární klíč jiné tabulky a tvoří vztahy.</li>
          </ul>
        </div>
        <div class="image-wrapper">
          <img src="https://media.geeksforgeeks.org/wp-content/uploads/20250111112649494919/relational_model.webp" alt="Relational model illustration">
        </div>
      </div>
      
      <div class="notice">
        <strong>SQL (Structured Query Language)</strong> je standardní jazyk pro práci s relačními databázemi – pro vytváření, čtení, aktualizaci a mazání dat.
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Srovnání: SQL vs. NoSQL</h2>
      <p>Volba mezi relačními a nerelačními databázemi závisí na konkrétních požadavcích projektu. Obě technologie mají své místo v moderní architektuře.</p>
      
      <div class="comparison-grid">
        <div class="comparison-card sql-card">
          <div class="card-header">
            <h3>SQL (Relační)</h3>
          </div>
          <ul class="styled-list">
            <li>Strukturovaná data, tabulky</li>
            <li>Pevné schéma</li>
            <li>Silná integrita dat (ACID transakce)</li>
            <li>Škálování spíše vertikální</li>
            <li><strong>Příklady:</strong> MySQL, PostgreSQL, Oracle</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card">
          <div class="card-header">
            <h3>NoSQL (Nerelační)</h3>
          </div>
          <ul class="styled-list">
            <li>Nestrukturovaná (JSON dokumenty, grafy, atd.)</li>
            <li>Flexibilní schéma</li>
            <li>Distribuované, horizontální škálování</li>
            <li>Přednost má výkon před striktním ACID</li>
            <li><strong>Příklady:</strong> MongoDB, Cassandra, Redis</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Fáze návrhu databáze</h2>
      <p>Návrh databáze je iterativní proces, který zahrnuje několik klíčových fází od analýzy požadavků až po implementaci.</p>
      
      <div class="steps-container">
        <div class="step-item">
          <div class="step-number">1</div>
          <div class="step-content">
            <h4>Analýza požadavků</h4>
            <p>Definování účelu databáze, sběr informací a požadavků uživatelů.</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number">2</div>
          <div class="step-content">
            <h4>Konceptuální návrh</h4>
            <p>Vytvoření ER diagramu (Entity-Relationship) – vizuální reprezentace entit a jejich vztahů.</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number">3</div>
          <div class="step-content">
            <h4>Logický návrh</h4>
            <p>Transformace ER diagramu do relačního modelu a normalizace (odstranění redundance).</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number">4</div>
          <div class="step-content">
            <h4>Fyzický návrh</h4>
            <p>Specifikace datových typů, indexů a tvorba SQL pro konkrétní databázový stroj (DBMS).</p>
          </div>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Normalizace databáze</h2>
      <p>Normalizace je proces organizace sloupců a tabulek pro minimalizaci redundantních dat a zlepšení integrity dat. Rozlišujeme několik normálních forem (NF).</p>
      
      <div class="notice">
        Vyšší normalizované formy existují, ale 3. normální forma (3NF) je často dostatečná pro většinu aplikací.
      </div>
      
      <ul class="styled-list large-spacing">
        <li><strong>1. NF (First Normal Form):</strong> Žádné opakující se skupiny, všechny hodnoty ve sloupcích jsou atomické (dále nedělitelné).</li>
        <li><strong>2. NF (Second Normal Form):</strong> Splňuje 1. NF a všechny neprimární atributy jsou plně závislé na celém primárním klíči.</li>
        <li><strong>3. NF (Third Normal Form):</strong> Splňuje 2. NF a žádné neprimární atributy nejsou tranzitivně závislé na primárním klíči (závisí POUZE na klíči).</li>
      </ul>
      
      <div class="image-wrapper compact mt-4">
        <img src="https://miro.medium.com/0*vCmK7a4D4Qks6iM7.png" alt="Database normalization forms" style="background:#fff; padding:10px;">
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Základní SQL příkazy (CRUD)</h2>
      <p>CRUD je zkratka pro čtyři základní typy databázových operací: Create (Vytvořit), Read (Číst), Update (Aktualizovat) a Delete (Smazat).</p>

      <div class="code-blocks">
        <div class="code-block">
          <div class="code-header">Vytvoření tabulky (DDL)</div>
<pre><code>CREATE TABLE Zakaznici (
  ID INT PRIMARY KEY,
  Jmeno VARCHAR(50),
  Email VARCHAR(100)
);</code></pre>
        </div>
        
        <div class="code-block">
          <div class="code-header">Výběr dat (Read)</div>
<pre><code>SELECT Jmeno, Email 
FROM Zakaznici 
WHERE Jmeno = 'Jan Novák';</code></pre>
        </div>

        <div class="code-block">
          <div class="code-header">Vložení dat (Create)</div>
<pre><code>INSERT INTO Zakaznici (ID, Jmeno, Email) 
VALUES (1, 'Jan Novák', 'jan.novak@example.com');</code></pre>
        </div>

        <div class="code-block">
          <div class="code-header">Aktualizace dat (Update)</div>
<pre><code>UPDATE Zakaznici 
SET Email = 'novak.new@example.com' 
WHERE ID = 1;</code></pre>
        </div>
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

.info-box {
  background: rgba(59, 130, 246, 0.1);
  border-left: 4px solid var(--color-primary);
  padding: 1.5rem;
  border-radius: 0 var(--radius-md) var(--radius-md) 0;
  margin: 1.5rem 0;
}

.info-box p:last-child {
  margin-bottom: 0;
}

.image-wrapper {
  margin: 1.5rem 0;
  border-radius: var(--radius-md);
  overflow: hidden;
  box-shadow: var(--shadow-md);
  border: 1px solid var(--color-border);
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

.grid-2-col, .two-columns-layout, .comparison-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  align-items: center;
  margin: 1.5rem 0;
}

@media (max-width: 768px) {
  .grid-2-col, .two-columns-layout, .comparison-grid {
    grid-template-columns: 1fr;
  }
}

.chart-container {
  position: relative;
  height: 250px;
  width: 100%;
  background: rgba(15, 23, 42, 0.5);
  border-radius: var(--radius-md);
  padding: 1rem;
  border: 1px solid var(--color-border);
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

.styled-list.large-spacing li {
  margin-bottom: 1.25rem;
}

.styled-list li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: var(--color-primary);
  font-weight: bold;
}

.notice {
  background: rgba(139, 92, 246, 0.1);
  border: 1px dashed var(--color-accent);
  padding: 1.25rem;
  border-radius: var(--radius-md);
  margin: 1.5rem 0;
  color: #e2e8f0;
}

/* Comparison Cards */
.comparison-card {
  background: rgba(15, 23, 42, 0.6);
  border-radius: var(--radius-md);
  padding: 1.5rem;
  height: 100%;
  border: 1px solid var(--color-border);
}

.sql-card {
  border-top: 4px solid var(--color-primary);
}

.nosql-card {
  border-top: 4px solid var(--color-accent);
}

.card-header h3 {
  margin-top: 0;
  font-size: 1.25rem;
}

/* Steps Pipeline */
.steps-container {
  display: flex;
  flex-direction: column;
  margin: 2rem 0;
}

.step-item {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  position: relative;
}

.step-number {
  width: 40px;
  height: 40px;
  min-width: 40px;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.2rem;
  box-shadow: 0 0 15px rgba(59, 130, 246, 0.4);
  z-index: 2;
}

.step-content {
  background: rgba(255, 255, 255, 0.03);
  padding: 1.25rem;
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border);
  flex: 1;
}

.step-content h4 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  color: var(--color-primary-hover);
}

.step-content p {
  margin-bottom: 0;
  font-size: 0.95rem;
}

.connector {
  margin-left: 19px; /* center of the 40px circle */
  width: 2px;
  height: 25px;
  background: linear-gradient(to bottom, var(--color-primary), var(--color-accent));
  z-index: 1;
}

/* Code Blocks */
.code-blocks {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

@media (max-width: 768px) {
  .code-blocks {
    grid-template-columns: 1fr;
  }
}

.code-block {
  background: rgba(0, 0, 0, 0.4);
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border);
  overflow: hidden;
}

.code-header {
  background: rgba(255, 255, 255, 0.05);
  padding: 0.5rem 1rem;
  font-size: 0.85rem;
  font-family: monospace;
  color: var(--color-text-muted);
  border-bottom: 1px solid var(--color-border);
}

.code-block pre {
  margin: 0;
  border: none;
  background: transparent;
}
</style>
