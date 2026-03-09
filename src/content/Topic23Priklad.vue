<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Kódování ukázkového tlačítka</h2>
      <p>Sílu propojení HTML a CSS na jednoduché komponentě hezky ilustruje naprogramování vlastního tlačítka, na kterém jste zrovna teď sami klikli, abyste zobrazili tuto stránku.</p>
      
      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card sql-card" style="border-top-color: #e34c26;">
          <div class="card-header">
            <h3>Krok 1: HTML Element</h3>
          </div>
          <div class="sql-terminal" style="margin-top: 1rem; border-radius: 4px;">
<pre style="margin:0; padding: 10px;"><code><span style="color: #64748b;">&lt;</span><span style="color: #e34c26;">button</span> <span style="color: #3b82f6;">class</span><span style="color: #64748b;">=</span><span style="color: #10b981;">"moje-tlacitko"</span><span style="color: #64748b;">&gt;</span>
  Klikni Zde!
<span style="color: #64748b;">&lt;/</span><span style="color: #e34c26;">button</span><span style="color: #64748b;">&gt;</span></code></pre>
          </div>
          <p style="margin-top: 1rem; color: #94a3b8;">Samotné HTML dělá z tlačítka jen nevzhledný šedý obdelník 90. let nakreslený systémem, kterému jsme logicky přiřadili text, ale nulový feeling.</p>
          <div style="text-align: center; margin-top: 1rem;">
             <button style="all: revert;">Klikni Zde!</button>
          </div>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #264de4;">
          <div class="card-header">
            <h3>Krok 2: CSS Stylování</h3>
          </div>
          <div class="sql-terminal" style="margin-top: 1rem; border-radius: 4px;">
<pre style="margin:0; padding: 10px;"><code><span style="color: #eab308;">.moje-tlacitko</span> {
  <span style="color: #60a5fa;">background-color</span>: <span style="color: #10b981;">#10b981</span>;
  <span style="color: #60a5fa;">color</span>: <span style="color: white;">white</span>;
  <span style="color: #60a5fa;">border</span>: <span style="color: #f59e0b;">none</span>;
  <span style="color: #60a5fa;">border-radius</span>: <span style="color: #f59e0b;">8px</span>;
  <span style="color: #60a5fa;">padding</span>: <span style="color: #f59e0b;">10px 20px</span>;
  <span style="color: #60a5fa;">cursor</span>: <span style="color: #f59e0b;">pointer</span>;
  <span style="color: #60a5fa;">transition</span>: <span style="color: #f59e0b;">all 0.3s</span>;
}
<span style="color: #eab308;">.moje-tlacitko</span>:<span style="color: #f472b6;">hover</span> {
  <span style="color: #60a5fa;">background-color</span>: <span style="color: #10b981;">#059669</span>;
  <span style="color: #60a5fa;">transform</span>: <span style="color: #f59e0b;">scale(1.05)</span>;
}</code></pre>
          </div>
          <p style="margin-top: 1rem; color: #94a3b8;">CSS kaskáda naprosto převezme kontrolu. Změní barvy a hlavně, díky fázové pseudo-třídě <code>:hover</code> a nastavení přechodu <code>transition: 0.3s</code> zaručí plynulý barevný přechod po plynulém najetí myší.</p>
          <div style="text-align: center; margin-top: 1rem;">
             <button class="demo-btn">Klikni Zde!</button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';

.demo-btn {
  background-color: #10b981;
  color: white;
  border: none;
  font-size: 1rem;
  font-family: 'Inter', sans-serif;
  border-radius: 8px;
  padding: 10px 20px;
  cursor: pointer;
  transition: all 0.3s;
}

.demo-btn:hover {
  background-color: #059669;
  transform: scale(1.05);
}
</style>
