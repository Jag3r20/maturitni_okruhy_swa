<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Kybernetické hrozby a Malware</h2>
      <p>Škodlivý kód (Malicious Software = Malware) je každý program vytvořený s cílem poškodit počítač, ukrást data nebo získat neoprávněný přístup.</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <ul class="styled-list">
            <li><strong>Počítačový vir:</strong> Škodlivý kód, který se, podobně jako biologický vir, potřebuje připojit k hostiteli (jinému spustitelnému souboru), aby se mohl šířit.</li>
            <li><strong>Červ (Worm):</strong> Nepotřebuje hostitelský soubor. Šíří se po síti (internetu) zcela samostatně hledáním bezpečnostních děr.</li>
            <li><strong>Trojský kůň:</strong> Maskuje se jako užitečný program (např. hra nebo crack). Uživatel si ho sám dobrovolně nainstaluje, on v pozadí ale stahuje další malware.</li>
          </ul>
        </div>
        
        <div class="info-box danger">
          <h4 style="color: #ef4444;">Ransomware</h4>
          <p>Dnes nejnebezpečnější forma malwaru. Po nakažení <strong>zašifruje</strong> na disku všechny vaše soubory (fotky, dokumenty) a požaduje "výkupné" (ransom) v kryptoměnách za poskytnutí klíče k jejich odemčení.</p>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Sociální Inženýrství a Phishing</h2>
      <p>Často je slabším článkem zabezpečení člověk, nikoliv počítač. Útočníci raději obejdou firewally tak, že uživatele "přemluví", aby jim heslo dal dobrovolně.</p>
      
      <div class="notice">
        <strong>Phishing</strong> (rhybaření) je podvodná technika, kdy útočník rozesílá emaily, které vypadají jako od oficiální banky nebo e-shopu. E-mail obsahuje stresující tvrzení (např. "Vaše karta byla blokována, přihlaste se zde"). Odkaz vede na fiktivní stránku, kde útočník odchytí zadané přihlašovací údaje.
      </div>
    </section>
    
    <section class="glass-panel content-section">
      <h2>Zálohování (Backup) a principy</h2>
      <p>Jedinou 100% ochranou před smazáním nebo Ransomwarem je mít data fyzicky uložena a odpojena někde jinde.</p>
      
      <div class="steps-horizontal mt-4">
        <div class="step-box" style="border-top: 3px solid var(--color-primary);">
          <div class="step-num" style="font-size: 0.8em;">Full</div>
          <div class="step-text"><strong>Plná záloha</strong><br><span class="subtitle">Kopíruje vždy VŠECHNA data (Např. 100 GB). Pomalá, zabírá místo.</span></div>
        </div>
        <div class="step-arrow">|</div>
        <div class="step-box" style="border-top: 3px solid #f59e0b;">
          <div class="step-num" style="background: #f59e0b; font-size: 0.8em;">Inc</div>
          <div class="step-text"><strong>Inkrementální</strong><br><span class="subtitle">Zálohuje jen to, co se změnilo od <em>poslední libovolné</em> zálohy. Zabírá nejméně místa.</span></div>
        </div>
        <div class="step-arrow">|</div>
        <div class="step-box" style="border-top: 3px solid var(--color-accent);">
          <div class="step-num" style="background: var(--color-accent); font-size: 0.8em;">Diff</div>
          <div class="step-text"><strong>Diferenciální</strong><br><span class="subtitle">Zálohuje se vše, co se změnilo <em>od poslední PLNÉ</em> zálohy. Kompromis v rychlosti.</span></div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
