<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Práce v prezentačním programu</h2>
      <p>Nástroje pro tvorbu elektronických prezentací (Microsoft PowerPoint, Google Slides, Apple Keynote) slouží k <strong>vizuální podpoře mluveného slova</strong> řečníka. Cílem slajdu NENÍ suplovat čtecí dokument, ale upevnit pozornost diváka na klíčová slova, zatímco vnímá váš hlas a neverbální gesta.</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>Konstrukční prvky Prezentace</h3>
          <ul class="styled-list">
            <li><strong>Základní slajd:</strong> Tvořen titulkem (hlavní pointa), obrázkem nebo piktogramem, který emočně/logicky doplní slovo, a případně odrážkami doplňkových argumentů.</li>
            <li><strong>Předloha snímků (Master Slide):</strong> Tzv. "CSS prezentačních programů". Místo kopírování loga firmy na každý další snímek, umístí se jednou do předlohy a odtud se aplikuje všem budoucím listům automaticky. Zajišťuje absolutní sjednocení fontů a okrajů.</li>
            <li><strong>Přechody:</strong> Grafické efekty, ke kterým dojde při posunu z jednoho snímku na druhý. Vždy používáme jeden konzistentní, v jednoduchosti je síla (např. pouhé 'Zesvětlení'). Letící šachovnice působí neprofesionálně.</li>
            <li><strong>Animace:</strong> Pohyb uvnitř jediného platného snímku (příchozí šipky apod.). Používá se k postupnému odkrývání tezí, aby posluchači nečetli pátý řádek dřív, než jej řeknete nahlas.</li>
          </ul>
        </div>
        
        <div class="info-box danger">
          <h4>Vele-zrada: Kognitivní přehlcení!</h4>
          <p>Lidský mozek neumí číst text a <em>současně</em> poslouchat mluvící osobu – u obou těchto akcí je zapojené stejné řečové centrum (tzv. Wernickeova oblast).</p>
          <p>Tím, že na snímek překopírujete dvě plné věty textu, <strong>nutíce</strong> čtenáře číst. Po celou dobu, kdy čte (i když zrychleně), Vás mentálně vůbec neposlouchá a Váš hlas mu hlučí jen v pozadí jak Rádio!</p>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Pravidlo 5x5 a Zásady typografie</h2>
      <p>I pro prezentace existují nepsaná typografická dogmata, která se používají v profesionálním byznysu.</p>

      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card sql-card" style="border-top-color: #10b981;">
          <div class="card-header">
            <h3>Pravidlo maxima textu: 5x5 (či 6x6)</h3>
          </div>
          <p>
            Říká, že na jeden vizuální list nepatří maximálně více než 5 řádků (odrážek).
          </p>
          <ul class="styled-list custom-bullets">
            <li>Maximálně 5 řádků na jeden vizual na plátně.</li>
            <li>Maximálně 5 až 6 slov na každý daný řádek v bodu.</li>
            <li>Každé slovo nad limit okrádá publikum o Váš vzácný mluvený čas a ztěžuje čitelnost ze zadních lavic.</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #3b82f6;">
          <div class="card-header">
            <h3>Technický návrh písma</h3>
          </div>
          <p>
            Ačkoliv je u dokumentů (Bakalářka, Životopis) bezpatkové písmo chápáno jako hřích, u prezentací platí pravý opak!
          </p>
          <ul class="styled-list">
            <li><strong>Bezpatkové fonty (Sans Serif):</strong> Arial, Calibri, Helvetica, Open Sans. Přečtete je i z dálky 15 metrů bez toho, aniž by se litery slévaly v malátnou čáru.</li>
            <li><strong>Velikost:</strong> Nikdy pod 24 punktů! (Zpravidla 32 - 40pt pro texty a minimálně 48pt pro Nadpis).</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
