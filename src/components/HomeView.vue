<template>
  <div class="home-wrapper">
    <div class="glass-panel hero-section">
      <div class="hero-icon">🎓</div>
      <h1 class="hero-title">Příprava na Maturitu z IT</h1>
      <p class="hero-subtitle">Vítejte v interaktivní studijní pomůcce pro maturitní zkoušku z předmětu Informační technologie.</p>
      
      <div class="hero-grid">
        <div class="feature-card">
          <div class="icon">📚</div>
          <h3>15 Komplexních kapitol</h3>
          <p>Látka je rozdělena podle reálného maturitního sylabu, od fungování HW komponent až po stavbu webových stránek a projektové řízení.</p>
        </div>
        
        <div class="feature-card">
          <div class="icon">💻</div>
          <h3>Teorie v praxi</h3>
          <p>Každý okruh obsahuje nejen teoretický základ, ale vždy i záložku "Praktický příklad", kde je učivo demonstrováno na reálných scénářích či blocích kódu.</p>
        </div>
        
        <div class="feature-card">
          <div class="icon">🚀</div>
          <h3>Moderní pojetí</h3>
          <p>Zapomeňte na nudná skripta. Interaktivní testovací tlačítka, vizualizace databázových spojení či plnohodnotné ukázky HTML kaskád - vše máte před sebou.</p>
        </div>
      </div>
      
      <div class="cta-box">
        Jste připraveni začít? Vyberte si libovolný okruh v levém bočním panelu a pusťte se do studia! 
      </div>
    </div>
  </div>
</template>

<style scoped>
.home-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 80vh;
  padding: 2rem;
}

.hero-section {
  max-width: 900px;
  width: 100%;
  padding: 4rem 3rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero-icon {
  font-size: 4rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 0 20px rgba(59, 130, 246, 0.5));
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-10px) rotate(2deg); }
  100% { transform: translateY(0px) rotate(0deg); }
}

.hero-title {
  font-size: 3rem;
  font-weight: 800;
  margin: 0 0 1rem 0;
  background: linear-gradient(135deg, #fff 0%, #94a3b8 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  letter-spacing: -1px;
}

.hero-subtitle {
  font-size: 1.25rem;
  color: var(--color-text-muted);
  max-width: 600px;
  margin: 0 auto 3rem auto;
  line-height: 1.6;
}

.hero-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-bottom: 3rem;
}

@media (max-width: 800px) {
  .hero-grid {
    grid-template-columns: 1fr;
  }
}

.feature-card {
  background: rgba(15, 23, 42, 0.5);
  border: 1px solid rgba(255, 255, 255, 0.05);
  padding: 2rem 1.5rem;
  border-radius: var(--radius-lg);
  transition: all var(--transition-base);
}

.feature-card:hover {
  transform: translateY(-5px);
  background: rgba(30, 41, 59, 0.8);
  border-color: rgba(59, 130, 246, 0.3);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.feature-card .icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.feature-card h3 {
  font-size: 1.1rem;
  color: #e2e8f0;
  margin-top: 0;
  margin-bottom: 1rem;
}

.feature-card p {
  color: #94a3b8;
  font-size: 0.9rem;
  line-height: 1.5;
  margin: 0;
}

.cta-box {
  background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
  border: 1px solid rgba(59, 130, 246, 0.2);
  padding: 1.5rem;
  border-radius: var(--radius-md);
  color: #60a5fa;
  font-weight: 500;
  display: inline-block;
  animation: pulse 3s infinite;
}

@keyframes pulse {
  0% { box-shadow: 0 0 0 0 rgba(59, 130, 246, 0.4); }
  70% { box-shadow: 0 0 0 10px rgba(59, 130, 246, 0); }
  100% { box-shadow: 0 0 0 0 rgba(59, 130, 246, 0); }
}
</style>
