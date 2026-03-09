<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Praktická ukázka: Dobrý vs. Špatný Design</h2>
      <p>Teorii UX návrhu si můžeme ověřit v praxi porovnáním přístupů k designu formulářů pro sběr uživatelských dat.</p>
      
      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card sql-card" style="border-top-color: #10b981;">
          <div class="card-header">
            <h3>Dobrý UX/UI návrh (✓)</h3>
          </div>
          <div style="background: #1e293b; padding: 1rem; border-radius: 8px; margin-bottom: 1rem; border: 1px solid #10b981;">
            <label style="display: block; margin-bottom: 0.5rem; font-size: 0.9em; color: #94a3b8;">Emailová adresa</label>
            <input type="email" placeholder="vas@telefon.cz" style="width: 100%; padding: 0.75rem; border-radius: 4px; border: 1px solid #3b82f6; background: #0f172a; color: white;">
            <span style="display: block; margin-top: 0.5rem; font-size: 0.8em; color: #10b981;">Správně vyplněný email</span>
          </div>
          <ul class="styled-list custom-bullets">
            <li>Jasné a stručné popisky (štítky) vedle polí, ne jen plovoucí text (placeholder).</li>
            <li>Okamžitá zpětná vazba (validace dat ještě před odesláním).</li>
            <li>Dostatečný kontrast prvků tvořící jasnou hierarchii.</li>
            <li>Velké dotykové plochy pro tlačítka (mobile-friendly).</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #ef4444;">
          <div class="card-header">
            <h3>Špatný UX/UI návrh (✗)</h3>
          </div>
          <div style="background: #e2e8f0; padding: 1rem; border-radius: 8px; margin-bottom: 1rem; text-align: center;">
             <input type="text" placeholder="Vložte email" style="padding: 0.25rem; font-size: 0.8em; border: 1px solid #cbd5e1; background: #f8fafc; color: #333;">
             <div style="margin-top: 0.5rem; color: #ef4444; font-size: 0.7em;">ERROR: WRONG ENTRY</div>
          </div>
          <ul class="styled-list error-bullets">
            <li>Použití chabého kontrastu (šedý text na světlém pozadí zhoršuje čitelnost).</li>
            <li>Nejasná chybová hlášení ("WRONG ENTRY" neříká, *co* je špatně).</li>
            <li>Chybějící popisky (placeholdery zmizí, když uživatel začne psát).</li>
            <li>Skrytá nebo neočekávaná navigace ("klikněte ZDE").</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Od Wireframu k Prototypu</h2>
      
      <div class="steps-horizontal">
        <div class="step-box">
          <div class="step-num">1</div>
          <div class="step-text">Wireframe (Drátěný model)</div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box" style="border-color: #3b82f6;">
          <div class="step-num">2</div>
          <div class="step-text">Mockup (Vizuální návrh)</div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box" style="border-color: #10b981;">
          <div class="step-num">3</div>
          <div class="step-text">Prototyp (Interaktivní)</div>
        </div>
      </div>
      
      <div class="info-box">
        <strong>Vývojový cyklus v praxi:</strong> Nástroje jako <em>Figma</em> nebo <em>Adobe XD</em> umožňují designérům nejdříve černobíle seskládat rozložení aplikace (Wireframe), poté přidat barvy, obrázky a reálnou typografii (Mockup) a nakonec propojit obrazovky šipkami tak, aby aplikace fungovala jako reálná i bez znalosti skriptování (Prototyp pro uživatelské testování).
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
