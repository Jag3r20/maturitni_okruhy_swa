<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Generace počítačů</h2>
      <p>Historie počítačů se dělí do několika generací podle použitých základních elektronických součástek.</p>
      
      <div class="steps-horizontal">
        <div class="step-box">
          <div class="step-num">1.</div>
          <div class="step-text">Elektronky (40. léta)<br><span class="subtitle">ENIAC. Neefektivní, obrovské, kazivé.</span></div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box">
          <div class="step-num">2.</div>
          <div class="step-text">Tranzistory (50. léta)<br><span class="subtitle">Zmenšení rozměrů a spotřeby.</span></div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box">
          <div class="step-num">3.</div>
          <div class="step-text">Integ. obvody (60. léta)<br><span class="subtitle">Více součástek na jednom čipu.</span></div>
        </div>
        <div class="step-arrow">→</div>
        <div class="step-box">
          <div class="step-num">4.</div>
          <div class="step-text">Mikroprocesory (od 70. let)<br><span class="subtitle">Základ dnešních PC. CPU na čipu.</span></div>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Významné milníky (Kdo je kdo)</h2>
      <ul class="styled-list large-spacing">
        <li><strong>Z3 (Konrad Zuse) / Colossus:</strong> První plně funkční počítače z období 2. světové války.</li>
        <li><strong>ENIAC (1946):</strong> První univerzální, turing-kompletní, čistě elektronický počítač (vážil 27 tun).</li>
        <li><strong>Alan Turing:</strong> Otec teoretické informatiky, koncept Turingova stroje (abstraktní model počítače).</li>
        <li><strong>John von Neumann:</strong> Koncept architektury počítače (program a data ve stejné paměti) – 1945, standard dodnes.</li>
        <li><strong>Apple II (1977) a IBM PC (1981):</strong> Průlom na poli osobních počítačů (PC) pro domácnosti a kanceláře.</li>
      </ul>
    </section>

    <section class="glass-panel content-section">
      <h2>Moderní trendy v informatice</h2>
      
      <div class="grid-2-col align-start">
        <div class="info-box">
          <h4>Kvantové počítače (Quantum Computing)</h4>
          <p>Místo bitů (0, 1) pracují s q-bity, které mohou být v superpozici (nabývat obou stavů současně). Lze pomocí nich řešit extrémně složité výpočty, modely látek a kryptologii násobně rychleji než klasickými procesory.</p>
        </div>
        
        <div class="info-box accent">
          <h4>Vesmír věcí (Internet of Things - IoT)</h4>
          <p>Zapojení nejrůznějších běžných předmětů (žárovky, pračky, senzory) do sítě. Zařízení mezi sebou mohou komunikovat bez lidského zásahu (např. automatické vytápění dle polohy mobilu uživatele).</p>
        </div>

        <div class="info-box" style="border-color: #f59e0b; background: rgba(245, 158, 11, 0.1);">
          <h4 style="color: #f59e0b;">Umělá inteligence (AI) a Machine Learning (ML)</h4>
          <p>Schopnost strojů napodobovat lidské schopnosti pochopení. Strojové učení učí systémy odvozovat pravidla z obřího množství dat místo tradičního if-else programování.</p>
        </div>
        
        <div class="info-box" style="border-color: #10b981; background: rgba(16, 185, 129, 0.1);">
          <h4 style="color: #10b981;">Cloud Computing</h4>
          <p>Místo vlastnictví výkonného hardwaru a diskových polí si firma/uživatel pronajímá výpočetní výkon "jako službu" ze sítě vzdálených serverů (IaaS, PaaS, SaaS).</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
