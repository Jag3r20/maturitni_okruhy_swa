<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Praktická volba Licence</h2>
      <p>Představte si, že jste vytvořili užitečný program (např. aplikaci na úpravu fotek). Jak ho nabídnout světu?</p>
      
      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card sql-card" style="border-color: #3b82f6;">
          <div class="card-header">
            <h3>Scénář A: Chci na tom vydělat</h3>
          </div>
          <p>
            Vydáte <strong>Shareware (Trial verzi)</strong>.
          </p>
          <ul class="styled-list">
            <li>Lidé si stáhnou aplikaci zdarma. Mohou ji používat 30 dní, ale na uloženou fotku vloží aplikace vodoznak.</li>
            <li>Souběžně jim nabídnete <strong>zakoupení licenčního klíče</strong>.</li>
            <li>Klíč odstraní vodoznak a změní statut z Trialu na Plnou Komerční Verzi. Program samotný je proprietární (uzavřený).</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card" style="border-color: #10b981;">
          <div class="card-header">
            <h3>Scénář B: Chci pomoci komunitě</h3>
          </div>
          <p>
            Vydáte kód na GitHubu pod <strong>MIT nebo GNU GPL</strong>.
          </p>
          <ul class="styled-list custom-bullets">
            <li>Aplikace je zdarma. Kdokoliv ze světa vám může nahlásit chybu, nebo vám přes tzv. Pull Request kódem přímo pomoci ji vylepšit.</li>
            <li>Budujete si silné jméno a portfolio (což ocení např. budoucí zaměstnavatel).</li>
            <li>Lze vybírat dobrovolné dary (Donationware).</li>
          </ul>
        </div>
      </div>

      <div class="notice">
        <strong>Pojmy k pamatování:</strong> "Free" v angličtině u softwaru znamená buď "Free as in beer" (zmrzlina zdarma - neplatíte, Freeware) nebo "Free as in speech" (svoboda projevu - můžete se kódem zabývat, Open-source).
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
