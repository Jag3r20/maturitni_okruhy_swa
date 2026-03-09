<script setup>
defineProps({
  topics: {
    type: Array,
    required: true
  },
  selectedId: {
    type: [Number, String],
    required: true
  }
})

defineEmits(['select'])
</script>

<template>
  <aside class="sidebar glass-panel">
    <div class="sidebar-header">
      <h2>Maturita INF</h2>
      <p class="subtitle">Přehled okruhů</p>
    </div>
    
    <nav class="sidebar-nav">
      <ul>
        <li class="nav-item">
          <button 
            class="nav-btn" 
            :class="{ active: selectedId === 'home' }"
            @click="$emit('select', 'home')"
            style="margin-bottom: 1rem; background: linear-gradient(90deg, rgba(59, 130, 246, 0.1) 0%, transparent 100%); border-left: 2px solid var(--color-primary);"
          >
            <span class="topic-id" style="font-size: 1.2em; opacity: 1;">🏠</span>
            <span class="topic-title" style="font-weight: bold; color: #60a5fa;">Úvodní obrazovka</span>
          </button>
        </li>
        <li 
          v-for="topic in topics" 
          :key="topic.id"
          class="nav-item"
        >
          <button 
            class="nav-btn" 
            :class="{ active: topic.id === selectedId }"
            @click="$emit('select', topic.id)"
          >
            <span class="topic-id">{{ topic.id }}.</span>
            <span class="topic-title">{{ topic.title }}</span>
          </button>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<style scoped>
.sidebar {
  width: var(--sidebar-width);
  height: calc(100vh - 3rem); /* Očištěno o padding */
  position: sticky;
  top: 1.5rem;
  left: 0;
  display: flex;
  flex-direction: column;
  padding: 1.5rem 1rem;
  border-radius: var(--radius-lg); /* Zpět oblý roh! */
  z-index: 10;
}

.sidebar-header {
  margin-bottom: 2rem;
  padding: 0 0.5rem;
}

.sidebar-header h2 {
  font-size: 1.5rem;
  margin: 0;
  background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 700;
  border: none;
}

.subtitle {
  font-size: 0.875rem;
  margin: 0;
  opacity: 0.8;
}

.sidebar-nav {
  flex: 1;
  overflow-y: auto;
  padding-right: 0.5rem;
}

/* Custom scrollbar just for sidebar */
.sidebar-nav::-webkit-scrollbar {
  width: 4px;
}
.sidebar-nav::-webkit-scrollbar-thumb {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 4px;
}
.sidebar-nav::-webkit-scrollbar-thumb:hover {
  background: rgba(255, 255, 255, 0.2);
}

.sidebar-nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  margin-bottom: 0.5rem;
}

.nav-btn {
  width: 100%;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.85rem 1rem;
  background: transparent;
  border: 1px solid transparent;
  color: var(--color-text-muted);
  font-size: 0.95rem;
  font-weight: 500;
  border-radius: var(--radius-md);
  cursor: pointer;
  transition: all var(--transition-fast);
  text-align: left;
}

.nav-btn:hover {
  background: rgba(255, 255, 255, 0.03);
  color: var(--color-text);
  transform: translateX(6px);
}

.nav-btn.active {
  background: linear-gradient(90deg, var(--color-accent-subtle) 0%, transparent 100%);
  border-color: rgba(168, 85, 247, 0.2);
  color: #fff;
  box-shadow: inset 3px 0 0 var(--color-accent);
}

.topic-id {
  color: var(--color-accent);
  font-weight: 700;
  opacity: 0.8;
  transition: color var(--transition-fast);
}

.nav-btn.active .topic-id {
  opacity: 1;
  color: var(--color-primary-hover);
  text-shadow: 0 0 10px rgba(96, 165, 250, 0.5);
}
</style>
