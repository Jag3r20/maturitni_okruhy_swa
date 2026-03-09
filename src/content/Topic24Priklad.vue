<template>
  <div class="topic-content-wrapper">
    <section class="glass-panel content-section">
      <h2>Příklad sítě (API Přemostění)</h2>
      <p>O dynamických stránkách toho bylo řečeno spousta. Pojďme si nyní reálně zkusit kliknout na tlačítko a zavolat Backend po síti (Změřit jeho zpoždění = Ping). Toto tlačítko pošle HTTP požadavek přes celý svět nějakému cizímu serveru a počká si na Data v JSONu (Odpověď).</p>
      
      <div style="text-align: center; margin: 2rem 0;">
        <button @click="fetchRandomUser" :disabled="loading" class="action-btn">
          {{ loading ? '📡 Vytáčím server (Čekej prosím...)' : '⚡ Stáhni mi nového uživatele z Webu!' }}
        </button>
      </div>
      
      <div v-if="user" class="info-box success-box" style="display: flex; gap: 1rem; align-items: center; max-width: 600px; margin: 0 auto; background: rgba(30,41,59,0.9); border: 2px solid #10b981;">
        <img :src="user.picture.large" alt="Profil IT experta z API" style="width: 100px; height: 100px; border-radius: 50%; box-shadow: 0 0 10px rgba(16,185,129,0.5);" />
        <div>
          <h4 style="margin: 0; color: #10b981; font-size: 1.2rem;">{{ user.name.first }} {{ user.name.last }}</h4>
          <p style="margin: 0; color: #94a3b8; font-size: 0.9em; margin-top: 5px;">Město: <strong>{{ user.location.city }}, {{ user.location.country }}</strong></p>
          <p style="margin: 0; color: #e2e8f0; font-size: 0.85em; margin-top: 3px;">📧 {{ user.email }}</p>
          <p style="margin: 0; color: #f59e0b; font-size: 0.8em; margin-top: 5px;">⏱ Databáze odpověděla za: {{ measureTime }} ms</p>
        </div>
      </div>
      
      <div class="notice" style="margin-top: 2rem;">
        Při každém kliku odesílá <strong>Frontend</strong> tajnou obálku (Fetch požadavek) mimo tuto aplikaci. Narazí na Server aplikaci jménem <em>RandomUser.me</em>. Její <strong>Backend</strong> vygeneruje ze své SQL databáze záznam a zapíše ho do JSONu a balíček vrátí zpět vám do prohlížeče. Náš JS tento JSON čte a vypisuje fotku a křestní jméno na kostru webu bez aktualizace stránky (SPA - Single Page Application chování).
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const user = ref(null)
const loading = ref(false)
const measureTime = ref(0)

const fetchRandomUser = async () => {
  loading.value = true
  const start = performance.now()
  try {
    const response = await fetch('https://randomuser.me/api/')
    const data = await response.json()
    user.value = data.results[0]
  } catch (error) {
    console.error("Networking Error:", error)
  } finally {
    const end = performance.now()
    measureTime.value = Math.round(end - start)
    loading.value = false
  }
}
</script>

<style scoped>
@import './topic-styles.css';

.action-btn {
  background: linear-gradient(135deg, var(--color-primary) 0%, #2563eb 100%);
  color: white;
  border: none;
  font-size: 1.1rem;
  font-weight: 600;
  padding: 15px 30px;
  border-radius: var(--radius-lg);
  cursor: pointer;
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.4);
  transition: all var(--transition-base);
}

.action-btn:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(59, 130, 246, 0.6);
}

.action-btn:disabled {
  opacity: 0.7;
  cursor: wait;
}
</style>
