<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Základní principy počítačových sítí</h2>
      <p>Počítačová síť je spojení dvou nebo více počítačů za účelem sdílení dat nebo prostředků (např. tiskárny). Sítě se dělí podle své velikosti a dosahu.</p>
      
      <div class="comparison-grid align-start mt-4">
        <div class="comparison-card sql-card" style="border-top-color: #f59e0b;">
          <div class="card-header">
            <h3>LAN (Local Area Network)</h3>
          </div>
          <p>Místní (lokální) počítačová síť.</p>
          <ul class="styled-list">
            <li>Omezený dosah: jedna budova, kancelář, domov.</li>
            <li>Typicky zapojená přes switch (přepínač) kabelem nebo bezdrátově přes Wi-Fi router.</li>
            <li>Nejvyšší rychlost přenosu, minimální zpoždění (latence).</li>
          </ul>
        </div>
        
        <div class="comparison-card nosql-card" style="border-top-color: #3b82f6;">
          <div class="card-header">
            <h3>WAN (Wide Area Network)</h3>
          </div>
          <p>Rozlehlá (globální) síť počítačových podsítí.</p>
          <ul class="styled-list">
            <li>Spojuje různé LAN po celém světě.</li>
            <li>Nejznámější a největší veřejnou WAN sítí je <strong>Internet</strong> samotný.</li>
            <li>Využívá infrastrukturu poskytovatelů (ISP - O2, Vodafone atd.) do optických i bezdrátových uzlů.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="glass-panel content-section">
      <h2>Služby Internetu</h2>
      <p>Internet není jen "prohlížení webu". Internet (samotná HW/SW struktura propojující světovou infrastrukturu rodiny protokolů TCP/IP) přenáší data pro celou řadu různorodých služeb, které rozeznáváme podle tzv. <em>čísla portů</em> (0-65535).</p>

      <div class="grid-2-col align-start mt-4">
        <div>
          <ul class="styled-list large-spacing">
            <li><strong>WWW (World Wide Web):</strong> Służba běžící po HTTP (Port 80) a šifrovaném HTTPS (Port 443). Stará se o přenos webových stránek tvořených kódem HTML.</li>
            <li><strong>E-mail (SMTP/IMAP):</strong> Zajišťuje odesílání zpráv od klienta k serveru (Simple Mail Transfer Protocol, Port 25) a čtení zpráv (Port 143/993).</li>
            <li><strong>DNS (Domain Name System):</strong> "Zlaté stránky internetu". Překládá URL adresy jako <em>www.seznam.cz</em> na strojově obsluhovanou IP adresu <em>77.75.79.53</em>, aby ji servery mohly najít po fyzické trase kabelů.</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4>Vyslovujeme správně IP Adresu (IPv4)</h4>
          <p>V síti LAN i WAN na internetu jsme definování takzvanou IP adresou. Jde o 32-bitové číslo zapisované ve formátu 4 x 8 bitů, které nabývá hodnoty 0 - 255. Zápis může být například:</p>
          <p><code>192.168.1.130</code> (typická lokální privátní adresa telefonu získána přes DHCP od domácího Wi-Fi routeru).</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
