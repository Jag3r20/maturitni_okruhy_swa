<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Analýza sestavy PC</h2>
      <p>V praxi se málokdy setkáváme jen s holým teoretickým popisem součástek. Častěji musíme dekódovat "letákové" nabídky z e-shopů. Pojďme si jednu rozebrat.</p>
      
      <div class="info-box accent" style="background: rgba(15, 23, 42, 0.8); border: 1px solid var(--color-border); border-left: 4px solid var(--color-accent);">
          <h3 style="color: #a78bfa; margin-bottom: 0;">Sestava: "Super Gamer Pro 2026"</h3>
          <p style="font-family: monospace; color: #94a3b8; font-size: 0.9em; margin-top: 0.5rem;">
            AMD Ryzen 5 7600 | 32 GB DDR5 | 1 TB M.2 SSD | NVIDIA RTX 4060 Ti 8GB
          </p>
      </div>
      
      <h3>Rozbor parametrů:</h3>
      <table style="width: 100%; border-collapse: collapse; margin-top: 1.5rem; text-align: left;">
        <thead>
          <tr style="border-bottom: 1px solid rgba(255,255,255,0.1); color: var(--color-primary-hover);">
            <th style="padding: 1rem;">Komponenta</th>
            <th style="padding: 1rem;">Dekódovaný význam</th>
            <th style="padding: 1rem;">Role v PC</th>
          </tr>
        </thead>
        <tbody>
          <tr style="border-bottom: 1px dashed rgba(255,255,255,0.05);">
            <td style="padding: 1rem;"><strong>CPU:</strong> AMD Ryzen 5 7600</td>
            <td style="padding: 1rem;">6 jader, moderní architektura. Značí zlatý střed procesorů (Ryzen 5 / Intel Core i5).</td>
            <td style="padding: 1rem;">Obstarává běh Windows, logiku her, fyziku a veškeré pokyny "navíc".</td>
          </tr>
          <tr style="border-bottom: 1px dashed rgba(255,255,255,0.05);">
            <td style="padding: 1rem;"><strong>GPU:</strong> RTX 4060 Ti 8GB</td>
            <td style="padding: 1rem;">Grafická karta s 8 GB VRAM (vlastní grafická paměť).</td>
            <td style="padding: 1rem;">Počítání polygonů, pixelů a textur pro monitor. Bez ní by plynulé hry nešly.</td>
          </tr>
          <tr style="border-bottom: 1px dashed rgba(255,255,255,0.05);">
            <td style="padding: 1rem;"><strong>RAM:</strong> 32 GB DDR5</td>
            <td style="padding: 1rem;">Nadstandardní velikost v nejnovějším rychlém standardu (DDR5).</td>
            <td style="padding: 1rem;">Pojme všechny zapnuté tabulky v Chrome, načtenou mapu ve hře i editoru.</td>
          </tr>
          <tr>
            <td style="padding: 1rem;"><strong>Úložiště:</strong> 1 TB M.2 SSD</td>
            <td style="padding: 1rem;">Polovodičový disk typu NVMe namontovaný přímo na desce do slotu M.2.</td>
            <td style="padding: 1rem;">Zde je nainstalovaný systém a z této rychlosti závisí, jak rychle naběhne PC.</td>
          </tr>
        </tbody>
      </table>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
