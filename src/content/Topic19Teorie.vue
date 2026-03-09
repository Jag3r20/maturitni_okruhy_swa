<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Práce s textovým editorem (Word procesorem)</h2>
      <p>Aplikace ze skupiny <strong>Word procesorů</strong> slouží primárně pro tvorbu, formátování a tisk textových dokumentů. Nejznámějším zástupcem je komerční <em>Microsoft Word</em>, dále open-source <em>LibreOffice Writer</em> nebo cloudový <em>Google Docs</em>.</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>Základní pojmy a dělení textu</h3>
          <ul class="styled-list">
            <li><strong>Znak:</strong> Nejmenší jednotka (písmeno, číslo). Vlastností je řez a velikost písma (bold/kurzíva, arial, 12pt).</li>
            <li><strong>Slovo:</strong> Skupina znaků oddělena mezerami.</li>
            <li><strong>Odstavec:</strong> Blok textu zakončený klávesou <code>ENTER</code> (skrytý znak ¶). Nejdůležitější logická část dokumentu.</li>
            <li><strong>Dokument:</strong> Finální ucelení, určuje se okraj a orientace papíru na tisk (Formát A4, rozpětí).</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4>Zlatá pravidla psaní ve Wordu</h4>
          <ol class="styled-list custom-bullets" style="padding-left: 0;">
            <li>Nikdy nevytvářím odrážky "kreslením" pomlček za sebe. Použiji nástroj 'Seznam'.</li>
            <li>Nikdy nezarovnávám text mezerami (Mezerníkem) doprostřed okraje! Používám nástroj zarovnání na střed či 'Tabulátor'.</li>
            <li>Konec stránky nedělám zběsilým mačkáním 'Enter'. Vkládám klávesovou zkratkou skrytý <strong>Konec Stránky</strong> (CTRL+Enter).</li>
          </ol>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Formátování pomocí "Stylů"</h2>
      <p>Styles (Styly) oddělují fyzický <strong>obsah</strong> (to co píšu) od <strong>vzhledu</strong> (jak to má vypadat). Profesionální text má vždy hlavičky organizované Styly a ne ručním natíráním písma z černé na modrou.</p>
      
      <div class="sql-terminal" style="margin-top: 2rem;">
        <div class="sql-header">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
          <span class="title">Generování automatického obsahu dokumentu</span>
        </div>
<pre><code><span class="comment"># Pokud jsem dodržel dělení nadpisů v dokumentu strukturálně do Stylů (nadpisů velikostí H1 (Název), H2 (Kapitola), H3 (Podkapitola)):</span>

<span class="keyword">Reference -> Obsah -> Vytvořit obsah Tabulkou 1</span>

<span class="comment">1.  Úvod (Nadpis H1) ............................ str. 1
  1.1 Proč to píšu (Nadpis H2)................... str. 1
2.  Jádro Věci (Nadpis H1) ...................... str. 2</span>

<span class="comment"># Značná úspora času při psaní např. bakalářských prací. Kdykoliv se vloží text mezi sekce, číslování kapitol i stránek se posune samo plně automaticky!</span>
</code></pre>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
