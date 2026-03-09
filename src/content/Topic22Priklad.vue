<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Případová studie MS Access – Videopůjčovna</h2>
      <p>Vyzkoušejte si převod teoretického zadání problému malého obchodu na logiku Relační Databáze v MS Access pro tvorbu softwaru "Půjčovna".</p>
      
      <div class="info-box danger" style="background: rgba(30, 41, 59, 1); border-left: 4px solid var(--color-primary);">
        <h4 style="color: var(--color-primary-hover);">Úkol od zadavatele</h4>
        <p>"Potřebujeme systém, do kterého zaznamenáme informace o zákaznících (Pepa Novák) a filmech, které si vypůjčili a datum kdy to mají vrátit. Napište to celé třeba do jednoho archu ať je to vidět."</p>
      </div>

      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card nosql-card" style="border-top-color: #ef4444;">
          <div class="card-header">
            <h3>Špatně: Excelový způsob</h3>
          </div>
          <p>
            Vytvoříme gigantickou tabulku tak, ať vidí šéf na obrazovce přesně to, co chtěl:
          </p>
          <ul class="styled-list error-bullets" style="font-family: monospace; font-size: 0.9em; background: rgba(0,0,0,0.3); padding: 10px;">
            <li>Jméno | Přijmení | Adresa    | Film 1 | Film 2 | VracíDne</li>
            <li>Pepa  | Novák    | Krátká 12 | Shrek  | Matrix | 12.03.</li>
            <li>Pepa  | Novák    | Krátká 12 | Vetřel |        | 16.03.</li>
          </ul>
          <p style="color: #ef4444; font-weight: bold; margin-top: 10px;">Problém (Redundance): Pepa se přejmenuje a já ho budu muset ručně hledat a přepisovat na stonásobně místech!</p>
        </div>
        
        <div class="comparison-card sql-card" style="border-top-color: #10b981;">
          <div class="card-header">
            <h3>Správně: Access relační řešení</h3>
          </div>
          <p>Data rozsekáme na nezávislé ostrůvky spojené ID vazbami (Relace).</p>
          <ol class="styled-list custom-bullets" style="padding-left: 0;">
            <li><strong>Tabulka T_Zakaznici:</strong> (<em>ID_Zak: 1</em>, Jméno: Pepa...)</li>
            <li><strong>Tabulka T_Filmy:</strong> (<em>ID_Film: 88</em>, Nazev: Shrek...)</li>
            <li><strong>Spojovací Tabulka T_Vypujcky:</strong> Uchovává vztah N:M. Její podoba v PC vypadá jako nesrozumitelné: [<em>ID_Transakce: 554, ID_Zak: 1, ID_Film: 88, VracíDne: 12.03</em>]</li>
          </ol>
          <p style="color: #10b981; font-weight: bold; margin-top: 10px;">Kouzlo Dotazů: Aby to šéf uměl přečíst, vytvořím mu v MS Access DOTAZ, který tahle strojní čísla za pochodu v RAM poskládá vizuálně dohromady jako spojitý text.</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
