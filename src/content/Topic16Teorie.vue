<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Co je to Operační systém (OS)?</h2>
      <p>Operační systém je základní <strong>systémový program</strong> v počítači. Funguje jako prostředník (překladatel) mezi hardwarovými komponentami, spuštěnými aplikacemi a koncovým uživatelem. Bez něj by byl počítač pouze bezužitečnou hromadou součástek.</p>
      
      <div class="steps-horizontal">
        <div class="step-box" style="border-bottom: 3px solid var(--color-primary);">
          <div class="step-text" style="text-align: center; width: 100%;"><strong>Aplikace & Uživatel</strong><br><span class="subtitle" style="margin-bottom: 0; padding-bottom: 0; border: none;">(Word, Hra, Prohlížeč)</span></div>
        </div>
        <div class="step-arrow">⟷</div>
        <div class="step-box" style="background: rgba(139, 92, 246, 0.2); border: 1px solid var(--color-accent);">
          <div class="step-text" style="text-align: center; width: 100%; color: #fff;"><strong>Operační systém (OS)</strong><br><span class="subtitle" style="margin-bottom: 0; padding-bottom: 0; border: none;">(Kernel, Shell, API)</span></div>
        </div>
        <div class="step-arrow">⟷</div>
        <div class="step-box" style="border-bottom: 3px solid #10b981;">
          <div class="step-text" style="text-align: center; width: 100%;"><strong>Hardware</strong><br><span class="subtitle" style="margin-bottom: 0; padding-bottom: 0; border: none;">(CPU, RAM, Disky)</span></div>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Hlavní úkoly OS</h2>
      
      <div class="grid-2-col align-start">
        <ul class="styled-list large-spacing">
          <li><strong>Správa procesů a paměti:</strong> OS přiděluje procesorový čas a operační paměť (RAM) jednotlivým běžícím aplikacím (multitasking) tak, aby si programy navzájem "nečmáraly" do dat.</li>
          <li><strong>Správa souborů:</strong> Zabezpečuje fyzický zápis na disk (používá systémy souborů, jako např. NTFS u Windows nebo ext4 u doménového Linuxu) a prezentuje uživateli srozumitelnou adresářovou stromovou strukturu.</li>
          <li><strong>Správa periferií:</strong> Pomocí speciálních menších programů (tzv. <em>ovladačů / driverů</em>) dokáže OS "mluvit" s tiskárnami, grafickou kartou, klávesnicí.</li>
          <li><strong>Uživatelské rozhraní:</strong> Poskytuje přístup - ať už pomocí GUI (Graphical User Interface s okny a ikonami) nebo pomocí CLI (příkazová řádka).</li>
        </ul>
        
        <div class="info-box">
          <h4>Jádro (Kernel)</h4>
          <p>Srdce operačního systému, úzce spolupracující primárně s hardwarem. Jádro načítá paměť, nastavuje prioritu spuštěných aplikací a chrání systém před zhroucením u tzv. chyb dělení nulou.</p>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Populární OS a rodiny zástupců</h2>
      
      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card sql-card" style="border-color: #3b82f6;">
          <div class="card-header">
            <h3>Windows (Microsoft)</h3>
          </div>
          <p>
            Vychází konstrukčně ze starších MS-DOS, nyní ve verzích jako Win 10, Win 11. Středobod mnoha firem a jasný vítěz na poli softwaru pro PC hry, kvůli kompatibilitě DirectX. Běží na rodině <strong>NT (New Technology)</strong> kernelů.
          </p>
        </div>
        
        <div class="comparison-card nosql-card" style="border-color: #8b5cf6;">
          <div class="card-header">
            <h3>UNIX/Linux a macOS</h3>
          </div>
          <p>
            Široká rodina odkazující se na podobné UNIXové základy, založené na oprávněních, souborech a stabilní struktuře do serverového nasazení nebo profesionálů. Linux (Ubuntu, Debian, Android) je open-source. macOS (Apple) je proprietární "obálka" na unixovém základu (Darwin).
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
