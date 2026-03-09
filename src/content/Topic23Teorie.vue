<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Základní stavební kameny Webu</h2>
      <p>Pro fungování webových stránek v prohlížeči je dnes naprostým standardem kombinace tří základních pilířů, které definují celkový zážitek uživatele z frontendu.</p>
      
      <div class="steps-horizontal mt-4">
        <div class="step-box" style="border-top: 3px solid #e34c26;">
          <div class="step-num" style="background: #e34c26;">HTML</div>
          <div class="step-text"><strong>Struktura (Kostra)</strong><br><span class="subtitle">Definuje, KDE se nachází nadpis h1, kde začíná odstavec a jak vypadá odkaz.</span></div>
        </div>
        <div class="step-arrow">+</div>
        <div class="step-box" style="border-top: 3px solid #264de4;">
          <div class="step-num" style="background: #264de4;">CSS</div>
          <div class="step-text"><strong>Vzhled (Kůže)</strong><br><span class="subtitle">Kaskádové styly vybírají HTML prvky a obarvují je a zarovnávají (např. vedle sebe).</span></div>
        </div>
        <div class="step-arrow">+</div>
        <div class="step-box" style="border-top: 3px solid #f7df1e;">
          <div class="step-num" style="background: #f7df1e; color: #333;">JS</div>
          <div class="step-text"><strong>Interaktivita (Svaly)</strong><br><span class="subtitle">JavaScript reaguje na kliknutí a animuje web bez nutnosti načítat novou stránku.</span></div>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Sémantický model a vývoj CSS</h2>
      
      <div class="grid-2-col align-start mt-4">
        <div class="info-box">
          <h4>Sémantické HTML5 (Smysl částí)</h4>
          <p>Ve starém HTML se celý web skládal ze záplavy desítek divů (<code>&lt;div id="hlavicka"&gt;</code>). Nové HTML5 zavedlo pro přehlednost a pro lepší SEO a čtečky tagy s významem: <code>&lt;header&gt;</code>, <code>&lt;main&gt;</code>, <code>&lt;footer&gt;</code>, <code>&lt;article&gt;</code>.</p>
        </div>
        
        <div class="info-box accent">
          <h4>Evoluce rozložení v CSS</h4>
          <p>
            Historicky se web "skládal" zmateně pomocí HTML Tabulek nebo plovoucích elementů (Float). Dnes na moderní rozložení používáme výhradně:
          </p>
          <ul class="styled-list custom-bullets" style="padding-left: 0;">
            <li><strong>Flexbox:</strong> Pro zarovnání prvků do jednoho směru (řádku nebo sloupce). Skvělé např. pro navigační menu.</li>
            <li><strong>CSS Grid:</strong> Pro kreslení složitých dvojrozměrných mřížek (layoutů článků), bez ohledu na tok zdrojového HTML kódu.</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
