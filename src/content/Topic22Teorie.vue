<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Desktopové databázové systémy</h2>
      <p>Databázové programy (jako <strong>Microsoft Access</strong> nebo Base v LibreOffice) představují mezistupeň mezi obyčejnou tabulkou v Excelu a plnohodnotným relačním SQL serverem (MySQL). Jsou to vizuální nástroje pro tvorbu databází primárně pro malé firmy a osobní využití.</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>Čtyři pilíře MS Access</h3>
          <ul class="styled-list">
            <li><strong>Tabulky:</strong> Místo, kde fyzicky leží data (seznam zaměstnanců, seznam oddělení). Má striktní strukturu datových typů (Číslo, Text).</li>
            <li><strong>Dotazy (Queries):</strong> Slouží k vyhledání a filtrování dat z více tabulek najednou (Tvorba spojení - JOIN) do jednoho náhledu na obrazovku.</li>
            <li><strong>Formuláře:</strong> Grafické uživatelské rozhraní (okno s tlačítky a prázdnými políčky), přes které laici plní Databázi (tabulky), aby do nich nemuseli zapisovat přímo.</li>
            <li><strong>Sestavy (Reports):</strong> Dokumenty připravené a zformátované přímo pro tisk na papír (faktury, výplatní pásky).</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4>Tabulka NEBO Databáze?</h4>
          <p>Rozdíl mezi Tabulkovým Excelem a Databázovým Accessem je ve vnitřní logice. Databáze vynucuje tzv. Prvotní klíč (Primary Key) a vztahy (1:1, 1:N). Místo kopírování názvu Města všude možně v Excelu se v Accessu Uloží jen ID Města <em>18</em> a pomocí relace se počítač doví, že je to "Praha". (Normalizace dat).</p>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>QBE (Query By Example)</h2>
      <p>Namísto programování SQL kódu, nabízejí desktopové systémy návrhové mřížky zvané QBE.</p>

      <div class="notice border-left">
        <strong>Princip:</strong> Technik si ze seznamu nakreslených tabulek myší přetáhne sloupce (Pole), která chce vidět (Jméno, Přijmení, Plat) do spodní mřížky. Do řádku "Kritéria" pod sloupec <em>Plat</em> pouze napíše např. <code>> 40000</code>. Program sám na pozadí zkompiluje strukturu SQL, sáhne na harddisk a na obrazovku mu po spuštění "Vrátí" požadovaný výsledek.
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
