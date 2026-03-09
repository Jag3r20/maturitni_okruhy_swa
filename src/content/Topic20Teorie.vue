<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Tabulkový procesor (Spreadsheet)</h2>
      <p>Nejrozšířenějším zástupcem tabulkových procesorů je Microsoft Excel či Google Spreadsheets. Slouží k uchovávání strukturovaných dat v matici, provádění složitých výpočtů, analýzy dat pomocí kontingenčních tabulek a tvorbě piktogramů (grafů).</p>
      
      <div class="grid-2-col align-start mt-4">
        <div>
          <h3>Logická stavba Excelu</h3>
          <ul class="styled-list">
            <li><strong>Buňka (Cell):</strong> Základní jednotka, identifikovaná sloupcem a řádkem (např. <code>B4</code>). Může obsahovat text, číslo, datum nebo Vzorec/Funkci.</li>
            <li><strong>List (Sheet):</strong> Pracovní plocha rovnice. Velký mřížkový sešit (až milion řádků).</li>
            <li><strong>Sešit (Workbook):</strong> Samotný `.xlsx` soubor, který obaluje více listů pohromadě.</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4>Vzorec vs. Funkce</h4>
          <p><strong>Vzorce</strong> začínají znakem <code>=</code> a tvoříme je ručně (např. <code>=A1+A2*3</code>).</p>
          <p><strong>Funkce</strong> jsou předpřipravené magické vzorečky přímo od Microsoftu, například <code>=SUMA(A1:A50)</code> nebo komplikovanější <code>=KDYŽ(A1>50; "Dospělý"; "Dítě")</code>.</p>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Rozdíl mezi relativním a absolutním odkazováním</h2>
      
      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card nosql-card" style="border-top-color: #3b82f6;">
          <div class="card-header">
            <h3>Relativní adresa (B2)</h3>
          </div>
          <p>
            Pokud buňku s odkazem <code>=B2*2</code> zkopíruji (roztáhnu křížkem) o jeden řádek níže, Excel <strong>sám posune</strong> i odkaz na <code>=B3*2</code>.
          </p>
          <p style="color: #94a3b8; font-size: 0.9em;">Použití: Chci aplikovat stejné DPH na celý sloupec s 10 000 produkty.</p>
        </div>
        
        <div class="comparison-card sql-card" style="border-top-color: #f59e0b;">
          <div class="card-header">
            <h3>Absolutní adresa ($B$2)</h3>
          </div>
          <p>
            Pokud do adresy vložím symbol dolaru pomocí klávesy F4 (<code>=$B$2*2</code>) a buňku roztáhnu dolů, <strong>Excel ji "uzamkne"</strong> a vždy se matematicky odkáže jen a pouze na B2, ať kopíruji kamkoli.
          </p>
          <p style="color: #94a3b8; font-size: 0.9em;">Použití: Buňka B2 obsahuje fixní Kurz eura (25 Kč), kterým násobím zbytek ceníku nezávisle na řádcích.</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
