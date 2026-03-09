<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Aplikované "Pravidlo 3-2-1"</h2>
      <p>Nejspolehlivější systém pro ochranu firemních i domácích dat se opírá o zlaté pravidlo zvané 3-2-1. Zkušený IT technik toto pravidlo zavede v každé firmě.</p>
      
      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card sql-card" style="border-top-color: #3b82f6;">
          <div class="card-header">
            <h3>3 Kopie dat</h3>
          </div>
          <p>
            Měli byste mít celkem TŘI kopie důležitých dat (včetně originálu). Pokud je soubor jen na jednom místě, je jako by neexistoval.
          </p>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #f59e0b;">
          <div class="card-header">
            <h3>2 Různá média</h3>
          </div>
          <p>
            Tyto kopie ukládejte na DVA různé typy úložišť.
          </p>
          <ul class="styled-list">
            <li>Nesmí to být dva disky ve stejném PC.</li>
            <li>Jeden může být např. interní SSD v PC, druhý izolovaný NAS server na stole (síťový disk), třetí externí USB disk.</li>
          </ul>
        </div>
        
        <div class="comparison-card sql-card" style="border-top-color: #10b981;">
          <div class="card-header">
            <h3>1 Kopie mimo budovu (Offsite)</h3>
          </div>
          <p>
            Jedna z kopií <strong>musí</strong> být umístěna v jiné lokalitě (geofyzicky jinde).
          </p>
          <ul class="styled-list custom-bullets">
            <li>Ochrana před: Požárem, potopou, krádeží kanceláře.</li>
            <li>Typicky se řeší přes zašifrovanou zálohu do spolehlivého Cloudového úložiště.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Scénář: Úder Ransomwaru</h2>
      <div class="info-box danger">
        <h4>Vteřina v čase: Pondělí 8:00</h4>
        <p>Účetní otevřela zfalšovaný email s fiktivním daňovým dokladem v příloze. Trojan nainstaluje <strong>Ransomware</strong>. Do pěti minut jsou všechny soubory na pevném disku jejího PC a připojeném firemním serveru zašifrované (*.locked).</p>
      </div>

      <h3>Proces obnovy podle 3-2-1</h3>
      <ol class="styled-list large-spacing" style="list-style-type: decimal;">
        <li><strong>Zastavení šíření:</strong> Technik okamžitě vytrhne síťový kabel napadeného PC, aby izoloval malware od zbytku budovy (serverů).</li>
        <li><strong>Smazání serveru:</strong> Servery zasažené tímto virem se zformátují (vymažou "do čista"). Rozšifrování hrubou silou na šifru typu AES-256 je za dobu našeho slunce nemožné a výkupné se nezaručuje (a nepodporuje zločince).</li>
        <li><strong>Návrat k bodu v čase:</strong> Šikovný technik má zavedené víkendové <em>Off-site zálohování</em>. Připojí se ke cloudovému disku a stáhne nedělní <em>Full Backup</em> firmy nezasažený virem. Data jsou na světě během odpoledne. Ztráta jsou pouze maily otevřené v den infekce.</li>
      </ol>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
