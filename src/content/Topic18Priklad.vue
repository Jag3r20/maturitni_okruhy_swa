<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Od URL textu až k vykreslení u vás na PC</h2>
      
      <div class="info-box" style="margin-bottom: 2rem;">
        <p><strong>Cílový stav:</strong> Jan chce otevřít ve svém prohlížeči (Chrome) stránku s videem na YouTube a zmáčkne klávesu <code>ENTER</code>. Co přesně se stane od kliknutí za 0.1s po síti mezi ním a serverem Youtube, který sídlí v Irsku?</p>
      </div>
      
      <div class="steps-container">
        <div class="step-item">
          <div class="step-number" style="background: #3b82f6;">1</div>
          <div class="step-content">
            <h4>Požadavek a dotaz na DNS</h4>
            <p>Prohlížeč rozezná text `www.youtube.com`. Nerozumí, jaké je to fyzické místo. Pošle proto přes UDP požadavek nejbližšímu <strong>DNS Serveru</strong> (od poskytovatele), kde se zeptá "Jaká je reálná IP Youtube?".</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number" style="background: #10b981;">2</div>
          <div class="step-content">
            <h4>Spojení (TCP Handshake) s IP: 142.250.74.206</h4>
            <p>DNS server obratem odpoví číselnou adresou. Z mobilu odejde signál na domácí router, odtamtud zašifrovaně k ISP anténě a přes optické kabely k podmořské bráně až k Google serveru (Irsko). Provede se proces 'Ahoj -> Ahoj -> Chci web', tedy "Handshake" a zahájí se HTTPS seance.</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number" style="background: #8b5cf6;">3</div>
          <div class="step-content">
            <h4>HTTP Request a HTTP Response</h4>
            <p>Spojení existuje. Prohlížeč Janovi aplikace zašle hlavičku `GET /watch?v=123`. Web Server (Youtube) vezme tento požadavek a sáhne do své databáze videí (viz. DBMS systém), najde příslušné video a sestaví HTML odpověď (kód webu).</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number" style="background: #f59e0b;">4</div>
          <div class="step-content">
            <h4>Packet rendering</h4>
            <p>Tato obrovská HTML odpověď (i s obrázky) se rozseká na milion stejných kostiček - <strong>Packetů</strong>. Po internetu je to jako na silnici, některý dorazí náklaďákem přes Paříž, jiný optikou po dně moře. Prohlížeč má ale číslované dílky (1,2,3). Vyčká, až dorazí všechny. Pokud jeden chybí (Drop), vyžádá jej znovu.</p>
          </div>
        </div>
        <div class="connector line-vertical"></div>
        <div class="step-item">
          <div class="step-number" style="background: #ef4444;">5</div>
          <div class="step-content">
            <h4>Zobrazení na obrazovce (Frontend)</h4>
            <p>Poslední střípek, tvořící celek - Prohlížeč stáhl HTML z Irských serverů a tzv. DOM strukturu začne aplikovat do paměti GPU PC a převede barevné čáry na rozhraní "Trubky". Celý proces trval lidským okem nezaznamenatelně 85 ms (milisekund).</p>
          </div>
        </div>
      </div>
      
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';

/* Dodatečná logika pro verlikélní steps z kopírky z Topic39Teorie.vue */
.steps-container {
  display: flex;
  flex-direction: column;
  margin: 2rem 0;
}

.step-item {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  position: relative;
}

.step-number {
  width: 40px;
  height: 40px;
  min-width: 40px;
  border-radius: 50%;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.2rem;
  box-shadow: 0 0 15px rgba(59, 130, 246, 0.4);
  z-index: 2;
}

.step-content {
  background: rgba(255, 255, 255, 0.03);
  padding: 1.25rem;
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border);
  flex: 1;
}

.step-content h4 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  color: var(--color-primary-hover);
}

.step-content p {
  margin-bottom: 0;
  font-size: 0.95rem;
}

.connector {
  margin-left: 19px; 
  width: 2px;
  height: 25px;
  background: rgba(255,255,255,0.2);
  z-index: 1;
}
</style>
