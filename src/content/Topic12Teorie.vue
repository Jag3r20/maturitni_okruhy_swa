<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Co je UX a UI?</h2>
      <p>Ačkoliv se zkratky UX a UI často používají společně, každá reprezentuje odlišnou (byť provázanou) disciplínu při návrhu digitálních produktů.</p>
      
      <div class="comparison-grid">
        <div class="comparison-card sql-card">
          <div class="card-header">
            <h3>UX (User Experience)</h3>
            <span class="subtitle">Uživatelská zkušenost</span>
          </div>
          <p>Zaměřuje se na to, <strong>jak produkt funguje</strong> a jaký pocit v uživateli zanechává.</p>
          <ul class="styled-list">
            <li>Uživatelský výzkum a persony</li>
            <li>Informační architektura</li>
            <li>Wireframing a prototypování</li>
            <li>Testování použitelnosti (usability testing)</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card">
          <div class="card-header">
            <h3>UI (User Interface)</h3>
            <span class="subtitle">Uživatelské rozhraní</span>
          </div>
          <p>Zaměřuje se na to, <strong>jak produkt vypadá</strong> a jak s ním uživatel vizuálně interaguje.</p>
          <ul class="styled-list">
            <li>Vizuální design a typografie</li>
            <li>Barvy, kontrast a branding</li>
            <li>Interaktivní prvky (tlačítka, animace)</li>
            <li>Responzivita a rozložení na displeji</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Základní principy dobrého UX/UI</h2>
      
      <div class="notice">
        Cílem dobrého designu je, aby se uživatel nemusel zamýšlet ("Don't Make Me Think").
      </div>

      <div class="grid-2-col align-start">
        <ul class="styled-list large-spacing">
          <li><strong>Konzistence:</strong> Stejné prvky by se měly chovat napříč celou aplikací stejně. Pokud je potvrzovací tlačítko zelené, mělo by být zelené všude.</li>
          <li><strong>Zpětná vazba (Feedback):</strong> Aplikace musí uživateli vždy sdělit, co se právě děje (např. načítací ikona, zpráva o úspěšném odeslání).</li>
          <li><strong>Hierarchie:</strong> Nejdůležitější informace a akce musí být vizuálně nejvýraznější (velikost, barva, umístění).</li>
          <li><strong>Přístupnost (Accessibility - a11y):</strong> Web by měl být použitelný i pre osoby se zrakovým nebo motorickým postižením (dostatečný kontrast, podpora čteček).</li>
        </ul>
        
        <div class="info-box accent">
          <h4>Heuristiky použitelnosti (Jakob Nielsen)</h4>
          <p>Sada 10 obecných pravidel pro návrh rozhraní. Například "Svoboda a kontrola uživatele" (možnost snadno zrušit/vrátit akci) nebo "Prevence chyb" (varování před vymazáním dat).</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
