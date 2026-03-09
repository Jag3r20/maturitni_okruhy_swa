<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Základní architektura PC</h2>
      <p>Dnešní počítače (PC, notebooky, mobily) vycházejí historicky z <strong>von Neumannovy architektury</strong>, která má pět hlavních komponent:</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
           <ul class="styled-list">
            <li><strong>Řídící jednotka:</strong> Řídí činnost všech částí počítače.</li>
            <li><strong>ALU (Aritmeticko-logická jednotka):</strong> Provádí matematické a logické operace.</li>
            <li><strong>Paměť:</strong> Uchovává právě vykonávaný program i data (RAM).</li>
            <li><strong>Vstupní zařízení:</strong> Klávesnice, myš, mikrofon.</li>
            <li><strong>Výstupní zařízení:</strong> Monitor, tiskárna, reproduktory.</li>
          </ul>
        </div>
        <div class="info-box">
          <h4>CPU (Centrální procesorová jednotka)</h4>
          <p>Spojuje Řídící jednotku a ALU do jednoho čipu. Je to "mozek" počítače, určující jeho nejdůležitější výkon. Měří se v taktu (např. 3.5 GHz - miliardy operací za vteřinu) a počtu jader.</p>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Rozdělení pamětí a jejich parametry</h2>
      
      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card sql-card" style="border-top-color: #f59e0b;">
          <div class="card-header">
            <h3>Operační paměť (RAM)</h3>
          </div>
          <p>
            Rychlá, těkavá (po vypnutí se maže). Slouží pro data spuštěných programů.
          </p>
          <ul class="styled-list">
            <li><strong>Kapacita:</strong> 8 GB – 32 GB u běžných PC.</li>
            <li><strong>Propustnost:</strong> Desítky GB/s.</li>
            <li><strong>Typy:</strong> DDR4, DDR5.</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #3b82f6;">
          <div class="card-header">
            <h3>Úložná paměť (Disk)</h3>
          </div>
          <p>
            Pomalejší, netěkavá (data zůstávají). Slouží k trvalému uchování souborů a OS.
          </p>
          <ul class="styled-list">
            <li><strong>Kapacita:</strong> 500 GB – 2 TB a více.</li>
            <li><strong>Rychlost:</strong> stovky MB/s (SATA) až tisíce MB/s (NVMe).</li>
            <li><strong>Typy:</strong> HDD (plotnový, pomalý), SSD (polovodičový, rychlý).</li>
          </ul>
        </div>
      </div>
      <div class="notice">
        <strong>Hierarchie pamětí:</strong> Čím blíž je paměť k CPU (např. L1/L2 Cache přímo v procesoru), tím je rychlejší, dražší a má menší kapacitu. Paměťové čipy na opačné straně (HDD) jsou nejlevnější v poměru cena/GB, ale velmi pomalé.
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
