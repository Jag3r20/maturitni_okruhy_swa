<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Slovo projektu a jeho znaky</h2>
      <p>Pokud jedete o víkendu nakoupit rohlíky a pak se vrátíte domů, není to projekt (je to proces nebo aktivita). Pokud se ale rozhodnete vykopat na zahradě 5-ti metrový bazén, pozvat si bagr a objednat filtraci, <strong>je to Projekt</strong>.</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>Znaky IT Projektu</h3>
          <ul class="styled-list">
            <li><strong>Unikátnost:</strong> Má jasný <em>Start</em> a <em>Konec</em>. Nikdy se neopakuje dvakrát identicky.</li>
            <li><strong>Cíl:</strong> Máme jasně definovaný konkrétní produkt (např. Vydání nového mobilního bankovnictví).</li>
            <li><strong>Zdroje:</strong> Omezený čas, peníze a lidé. Tvorbě aplikace se obvykle říká <em>Trojimperativ (Čas-Cena-Kvalita)</em>, kde ze tří bodů si můžete většinou vybrat pro splnění pouze dva za úkor třetího.</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4>Vedení Lidu (IT Role)</h4>
          <p>Typický tým v digitálním světě může tvořit např. trojice:</p>
          <ul class="styled-list custom-bullets" style="padding-left:0;">
            <li><em>Product Owner:</em> Zadavatel. Říká <strong>CO</strong> chce vyrobit (např. Banka).</li>
            <li><em>Developers:</em> Vykovávají černou programátorskou / designérskou práci. Vědí <strong>JAK</strong> to vyrobit.</li>
            <li><em>Project Manager / Scrum Master:</em> Stará se o to <strong>KDY a ZA KOLIK</strong> to bude a odstraňuje překážky (shání kávu a tiskne reporty pro vedení).</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Druhy metodik vývoje software</h2>
      
      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card sql-card" style="border-top-color: #3b82f6;">
          <div class="card-header">
            <h3>Tradiční postup (Vodopád - Waterfall)</h3>
          </div>
          <p>
            Vše se dopředu dokonale a absolutně naplánuje a až pak se začne naostro pracovat bez prostoru na chyby.
          </p>
          <div class="steps-horizontal" style="margin-top: 1rem;">
            <div class="step-num" style="background: transparent; color: white;">1. Analýza</div>
            <div class="step-arrow">→</div>
             <div class="step-num" style="background: transparent; color: white;">2. Design</div>
            <div class="step-arrow">→</div>
             <div class="step-num" style="background: transparent; color: white;">3. Vývoj</div>
            <div class="step-arrow">→</div>
             <div class="step-num" style="background: transparent; color: white;">4. Testování</div>
          </div>
          <p style="color: #ef4444; font-weight: bold; font-size: 0.9em; margin-top: 10px;">Nevýhoda: Pokud na konci ve 4. fázi klient řekne, že to chtěl růžové místo zelené, celý rok práce padá a začíná se od nuly z obrovskou finanční ztrátou.</p>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #10b981;">
          <div class="card-header">
            <h3>Agilní (Iterativní vývoj)</h3>
          </div>
          <p>
            Moderní přístup. Projekt se rozseká na měsíční bloky zvané <strong>Sprinty</strong>.
          </p>
          <ul class="styled-list custom-bullets">
            <li>Nenaplánuje se obří program pro banku na 5 let najednou, ale naplánuje se prvně jen "přihlašovací tlačítko" na dobu prvních 14 dní.</li>
            <li>Za 14 dní je hotové, vydá se, a klient jej může reálně používat a připomínkovat.</li>
            <li>Pokud chce klient "změnit barvu", práce 14-ti dnů se zahodí poměrně levně a projekt pokračuje bez rizika.</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
