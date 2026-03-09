<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Pravidlo DTP: Tok textu (Vdovy a sirotci)</h2>
      <p>Ve světě typografie (sazby textu na papír) bojují vydavatelé na stranách knih s grafickým problémem zvaným Vdovy a Sirotci. Moderní editory se to za vás snaží řešit.</p>
      
      <div class="comparison-grid align-start" style="margin-top: 2rem;">
        <div class="comparison-card sql-card" style="border-top-color: #ef4444;">
          <div class="card-header">
            <h3>Vdova 💔</h3>
          </div>
          <div style="background: white; padding: 1rem; color: black; border: 1px solid #ccc; font-family: 'Times', serif; margin-bottom: 1rem; box-shadow: 2px 2px 5px rgba(0,0,0,0.3);">
            <p style="text-indent: 10px; margin-top: 0;">Za devatero horama a devatero řekama žil jeden děda, který velmi velmi rád vyprávěl pohádky.</p>
            <p style="text-indent: 10px;">Byly to ale ty nejzajímavější příběhy a lidé je rádi poslouchali, zejména když napadl</p>
            <hr style="margin: 10px 0; border: none; border-bottom: 2px dashed #3b82f6;">
            <p style="margin-top: 10px; color: #ef4444; font-weight: bold;">sníh.</p>
          </div>
          <p>
            Jedno osamocené slovo, které zůstalo viset samo dole na řádku nebo dokonce přeteklo jako jedno jediné slovo na úplně novou stránku. (Vdova zůstala nakloněna dál sama.)
          </p>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #ef4444;">
          <div class="card-header">
            <h3>Sirotek 🧒</h3>
          </div>
          <div style="background: white; padding: 1rem; color: black; border: 1px solid #ccc; font-family: 'Times', serif; margin-bottom: 1rem; box-shadow: 2px 2px 5px rgba(0,0,0,0.3);">
            <p style="text-indent: 10px; margin-top: 0; color: #ef4444; font-weight: bold;">Jak šel čas tak se</p>
            <hr style="margin: 10px 0; border: none; border-bottom: 2px dashed #3b82f6;">
            <p style="margin-top: 10px;">král rozhodl opustit dům a všechny přihlížející. Měl k tomu velmi závažný důvod - došly rohlíky a bylo nutné nakoupit v nedalekém království.</p>
          </div>
          <p>
            Jeden řádek nového dlouhého odstavce, který začíná "blběčně" zcela osamocen dole u patičky strany a většina odstavce propadne na další stránku shora.
          </p>
        </div>
      </div>
      
      <div class="notice">
        Ve Wordu v sekci <strong>Odstavec (Paragraph)</strong> zapínáme funkci <em>Kontrola vdov a sirotků</em>. Word sám opticky zkrátí textové mezery v řádcích tak, aby přesunul chybějící slovo "na sílu" z druhé stránky zpět k rodině nahoru nebo naopak odsune půlku odstavce dolů, aby se nerozdělil graficky natřikrát.
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
