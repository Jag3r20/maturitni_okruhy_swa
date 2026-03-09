<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Příklad aplikací z praxe</h2>
      <p>Učebnicová definice trendů často nedokáže vystihnout reálný dopad. Zde je příklad toho, jak jsou současné technologie provázané.</p>
      
      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card sql-card" style="border-color: #8b5cf6; border-top-width: 4px;">
          <div class="card-header">
            <h3 style="color: #a78bfa;">Chytrá domácnost (IoT)</h3>
          </div>
          <p>
            V místnostech jsou teplotní senzory. Ty každé 2 vteřiny posílají data drobných datagramů.
          </p>
          <ul class="styled-list">
            <li>Nízký příkon energie.</li>
            <li>Okamžitá odezva v lokální síti.</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card" style="border-color: #3b82f6; border-top-width: 4px;">
          <div class="card-header">
            <h3 style="color: #60a5fa;">Cloud + AI analýza</h3>
          </div>
          <p>
            Sběr dat z milionu senzorů míří do Cloudového centra (např. AWS). Tam neuronová síť (AI) porovnává chování topení.
          </p>
          <ul class="styled-list">
            <li>AI navrhne uživateli do mobilu optimalizaci roční spotřeby účtu o 15 %.</li>
            <li>Náročný výpočet se děje v cloudu, nikoliv ve vašem mobilu.</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
