<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Architektura Klient-Server (Frontend a Backend)</h2>
      <p>Moderní webové aplikace se již neskládají (jako dříve) z desítek statických HTML souborů, se kterými nešlo pracovat (zanechat komentář atd). Dnešní "Dynamické" weby rozdělujeme na stranu uživatele a stranu serveru.</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>Frontend (Klient)</h3>
          <ul class="styled-list">
            <li><strong>Kde:</strong> Vykonává se v prohlížeči uživatele (Chrome, Safari).</li>
            <li><strong>Z čeho:</strong> HTML, CSS, JavaScript (Frameworky jako Vue, React).</li>
            <li><strong>Účel:</strong> Prezentovat data krásně pro lidské oko. Získávat data z tlačítek a formulářů. Rychlé reakce a animace, aniž by se musela obnovovat celá stránka (Technologie AJAX, SPA přístup - jako tento web!).</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4 style="color: var(--color-accent);">Backend (Server)</h4>
          <ul class="styled-list custom-bullets" style="padding-left: 0;">
            <li><strong>Kde:</strong> V datovém centru (skryto před uživatelem na IP adrese).</li>
            <li><strong>Z čeho:</strong> PHP, Python, Java, Node.js + Databáze (MySQL/MongoDB).</li>
            <li><strong>Účel:</strong> "Mozek a paměť aplikace". 100% zabezpečené ukládání zpráv do databáze, ověřování uživatelských hesel, logika bankovních převodů nebo generování souborů k tisku. Kód (např. PHP) běží jen u něj a klient si ho nemůže nikdy ukrást.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Programování a dynamický JS</h2>
      <p>Jakmile má web "paměť a vlastní uvažování", mluvíme o programovacích jazycích (např. JS na Frontend stranu nebo PHP na Backend stranu).</p>
      
      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card sql-card" style="border-top-color: #f7df1e;">
          <div class="card-header">
            <h3>Cyklus FOR (Opakování)</h3>
          </div>
          <p>
            Stroj umí věci tisíckrát zopakovat za zlomky vteřin. Nemusíme v HTML ručně 100x za sebou psát obrázek, napíšeme v JS jen smyčku <code>for</code>.
          </p>
          <div class="sql-terminal" style="border-radius: 4px;">
<pre style="margin:0; padding:10px;"><code><span style="color: #c678dd;">for</span> (<span style="color: #c678dd;">let</span> <span style="color: #e06c75;">i</span> <span style="color: #56b6c2;">=</span> <span style="color: #d19a66;">1</span>; i <span style="color: #56b6c2;">&lt;=</span> <span style="color: #d19a66;">100</span>; i<span style="color: #56b6c2;">++</span>) {
  <span style="color: #56b6c2;">console</span>.<span style="color: #61afef;">log</span>(<span style="color: #98c379;">`Uživatel ${i}`</span>);
}</code></pre>
          </div>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #ff2a2a;">
          <div class="card-header">
            <h3>Podmínka IF (Rozhodování)</h3>
          </div>
          <p>
            Dynamický web se zachová podle toho, jakou mají proměnné hodnotu. Pokud nejste přihlášeni, "Skryje (vymaže)" košík.
          </p>
           <div class="sql-terminal" style="border-radius: 4px;">
<pre style="margin:0; padding:10px;"><code><span style="color: #c678dd;">if</span> (uzivatel_prihlasen <span style="color: #56b6c2;">===</span> <span style="color: #d19a66;">true</span>) {
  <span style="color: #61afef;">ZobrazKosik</span>();
} <span style="color: #c678dd;">else</span> {
  <span style="color: #61afef;">VyvolejPrihlasovani</span>();
}</code></pre>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
