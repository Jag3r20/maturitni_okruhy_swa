<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Praktické ukázky pokročilejších funkcí</h2>
      <p>Umět napsat součet buněk umí každý. U maturity z IT se ale očekává znalost vyhledávacích tabulkových funkcí pro rozsáhlé systémy.</p>
      
      <div class="sql-terminal" style="margin-top: 2rem;">
        <div class="sql-header">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
          <span class="title">Svisť vyhledávání: VLOOKUP (SVYHLEDAT)</span>
        </div>
<pre><code><span class="comment"># Zadání: V obrovské tabulce zaměstnanců o 500 řádcích (od A2 do F500) chci 
# podle zadaného Rodného Čísla (uloženo v A1) rychle najít, 
# jakou má tento člověk na řádku hrubou mzdu (Mzda je ve 4. sloupci zleva).</span>

<span class="keyword">=SVYHLEDAT</span>(<span class="column">A1</span>; <span class="string">A2:F500</span>; <span class="table">4</span>; <span class="keyword">NEPRAVDA</span>)</code></pre>
      </div>

      <div class="grid-2-col align-start mt-4">
        <div class="info-box">
          <h4>Vysvětlení VLOOKUP syntaxe</h4>
          <ol class="styled-list" style="padding-left: 0;">
            <li><strong>A1</strong> - "Lookup Value" (Co hledáme, klíčový unikát).</li>
            <li><strong>A2:F500</strong> - "Table Array" (Kde hledáme, v matici záznamů).</li>
            <li><strong>4</strong> - "Col Index Num" (Který sloupec z vybrané matice má funkce vrátit nakonec zpět jako výsledek na obrazovku).</li>
            <li><strong>NEPRAVDA / 0 </strong> - Hledáme exaktní (přesnou) shodu klíče. Povolení "přibližné" (PRAVDA) se používá např. při přiřazení prospěchu studentovi z intervalu (1.5-2.0 = chvalitebný).</li>
          </ol>
        </div>
        
        <div class="info-box accent">
          <h4>Nové řešení: XLOOKUP</h4>
          <p>Novější verze MS Excel 365 integrují lepší náhradu jménem XLOOKUP. Nahrazuje zdlouhavé počítání sloupců (číslo 4) zleva a nevyžaduje, aby hledané ID bylo striktně vždy v prvním sloupci vlevo. Stačí jí předat pole pro klíč (A2:A500) a pole pro návrat (D2:D500).</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
