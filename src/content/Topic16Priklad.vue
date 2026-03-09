<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Příkazová řádka (CLI) vs Grafické GUI</h2>
      <p>I když dnes používáme primárně myš a grafická okna, všechny tyto akce se v jádře dají odeslat i přes textové rozhraní. Seznamte se s několika "kouzelnými" slovíčky správy OS (demonstrováno na Unix/Linux terminálu, Bash).</p>
      
      <div class="sql-terminal" style="margin-top: 2rem;">
        <div class="sql-header">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
          <span class="title">student@server:~$</span>
        </div>
<pre><code><span class="comment"># 1. Zobrazení aktuální polohy: Vytiskne cestu složky, ve které zrovna jsme (Print Working Directory)</span>
<span class="table">student@server:~$</span> <span class="keyword">pwd</span>
<span class="column">/home/student/Dokumenty</span>

<span class="comment"># 2. Vypsání obsahu složky: Zobrazí všechny soubory a složky uvnitř (List)</span>
<span class="table">student@server:~$</span> <span class="keyword">ls</span> <span class="column">-la</span>
<span class="column">drwxr-xr-x 2 student student 4096 bre 12 10:00 .
-rw-r--r-- 1 student student   42 bre 12 10:00 hesla.txt
drwxr-xr-x 4 student student 4096 bre 12 10:00 TajnaSlozka</span>

<span class="comment"># 3. Změna adresáře: Vstupme do uvnitř ležící složky TajnaSlozka (Change Directory)</span>
<span class="table">student@server:~$</span> <span class="keyword">cd</span> <span class="column">TajnaSlozka</span>

<span class="comment"># 4. Smazání souboru: Návrat nenávratně odstraní objekt "hesla.txt" (Remove)</span>
<span class="table">student@server:~/TajnaSlozka$</span> <span class="keyword">rm</span> <span class="column">hesla.txt</span></code></pre>
      </div>
      
      <div class="grid-2-col align-start mt-4">
        <div class="info-box">
          <h4>Výhody CLI (příkazů)</h4>
          <ul class="styled-list custom-bullets">
            <li>Lze je snadno řetězit a automatizovat (ve skriptech).</li>
            <li>Spotřebovávají řádově méně systémových prostředků (RAM, CPU).</li>
            <li>Rychlejší orientace na vzdáleném serveru po síti bez vizuálních zdržení.</li>
          </ul>
        </div>
        
        <div class="info-box accent">
          <h4>Příkazy v prostředí Windows (CMD, PowerShell)</h4>
          <ul class="styled-list">
            <li><code>dir</code> → Ekvivalent k <code>ls</code>.</li>
            <li><code>cd</code> → Funguje naprosto stejně pro změnu složky.</li>
            <li><code>md myfolder</code> → Vytvoř novou složku (Make Directory / mkdir v Linuxu).</li>
            <li><code>taskkill /F /PID 1240</code> → Sleng pro rychlé vynucené "zabití" zaseknuté aplikace z paměti.</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
@import './topic-styles.css';
</style>
