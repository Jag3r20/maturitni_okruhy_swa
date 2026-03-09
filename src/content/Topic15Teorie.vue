<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Základní rozdělení Software</h2>
      <p>Software (SW) je nehmotné vybavení počítače. Jedná se o sadu instrukcí, které říkají hardwaru, co má dělat. Dělí se primárně do tří kategorií:</p>
      
      <div class="steps-horizontal" style="margin-top: 2rem;">
        <div class="step-box" style="border-top: 3px solid var(--color-primary);">
          <div class="step-num">1</div>
          <div class="step-text"><strong>Systémový SW</strong><br><span class="subtitle">Zajišťuje chod samotného počítače a komunikaci s uživatelem. (Např. Windows, Linux, ovladače grafiky).</span></div>
        </div>
        <div class="step-arrow">+</div>
        <div class="step-box" style="border-top: 3px solid var(--color-accent);">
          <div class="step-num">2</div>
          <div class="step-text"><strong>Aplikační SW</strong><br><span class="subtitle">Programy určené pro konkrétní účel a práci uživatele. (Např. Word, Chrome, Počítačová hra).</span></div>
        </div>
        <div class="step-arrow">=</div>
        <div class="step-box" style="border-top: 3px solid #10b981;">
          <div class="step-num">3</div>
          <div class="step-text"><strong>Vývojové nástroje</strong><br><span class="subtitle">Programy pro tvorbu nových programů. (Kompilátory, VS Code).</span></div>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Licence: Způsoby šíření SW</h2>
      <p>Zakoupením softwaru si zpravidla nekupujete program samotný, ale <strong>právo (licenci)</strong> k jeho užití podle licenčního ujednání (EULA).</p>

      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>1. Proprietární (Komerční)</h3>
          <ul class="styled-list">
            <li>Kód je uzavřený a chráněný. Nesmíte ho upravovat ani prodávat dál.</li>
            <li><strong>Komerční SW:</strong> Platí se jednorázově (starý Office) nebo měsíčně jako předplatné (Adobe CC).</li>
            <li><strong>Shareware:</strong> Plná funkčnost omezena po zkušební dobu (Trial, 30 dní) nebo na omezené funkce, dokud nezaplatíte klíč.</li>
            <li><strong>Freeware:</strong> Můžete používat zcela zdarma, ale nemáte přístup ke kódu a nesmíte ho prodávat.</li>
          </ul>
        </div>
        <div>
          <h3>2. Otevřený kód (Open-source)</h3>
          <ul class="styled-list custom-bullets">
            <li>Zdrojový kód je veřejně dostupný. Kdo umí programovat, může program měnit.</li>
            <li>Většinou je <strong>zcela zdarma</strong> i pro komerční účely. Tvořen komunitami lidí z celého světa.</li>
            <li><strong>Vlivné licence:</strong> MIT, Apache, GNU GPL.</li>
            <li><em>Příklad:</em> Linuxový kernel, VLC Media Player, OBS Studio.</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
