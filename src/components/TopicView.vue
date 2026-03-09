<script setup>
import { computed, defineAsyncComponent, ref, watch } from 'vue'

const props = defineProps({
  topic: {
    type: Object,
    required: true
  }
})

const activeTab = ref('theory') // 'theory' | 'practice'

// Reset tab when topic changes
watch(() => props.topic.id, () => {
  activeTab.value = 'theory'
})

// Dynamically load the correct component based on topic ID and active tab
const CurrentComponent = computed(() => {
  const compName = activeTab.value === 'theory' ? 'Teorie' : 'Priklad'
  return defineAsyncComponent(() => 
    import(`../content/Topic${props.topic.id}${compName}.vue`).catch(() => {
      // Return a fallback component if not found
      return import('./NotFound.vue')
    })
  )
})
</script>

<template>
  <div class="topic-view">
    <header class="topic-header">
      <div class="topic-meta">Okruh č. {{ topic.id }}</div>
      <h1>{{ topic.title }}</h1>
      <p class="topic-summary" v-if="topic.summary">{{ topic.summary }}</p>
    </header>

    <div class="tabs-container">
      <div class="tabs-nav glass-panel">
        <button 
          class="tab-btn" 
          :class="{ active: activeTab === 'theory' }"
          @click="activeTab = 'theory'"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"></path><path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"></path></svg>
          Teoretická část
        </button>
        <button 
          class="tab-btn" 
          :class="{ active: activeTab === 'practice' }"
          @click="activeTab = 'practice'"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="16 18 22 12 16 6"></polyline><polyline points="8 6 2 12 8 18"></polyline></svg>
          Praktický příklad
        </button>
      </div>
    </div>

    <div class="topic-content">
      <Transition name="slide-fade" mode="out-in">
        <KeepAlive>
          <component :is="CurrentComponent" />
        </KeepAlive>
      </Transition>
    </div>
  </div>
</template>

<style scoped>
.topic-header {
  margin-bottom: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid var(--color-border);
}

.topic-meta {
  font-size: 0.875rem;
  color: var(--color-primary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.topic-header h1 {
  font-size: 2.5rem;
  margin-bottom: 0.75rem;
}

.topic-summary {
  font-size: 1.125rem;
  color: var(--color-text-muted);
  max-width: 800px;
}

.tabs {
  display: inline-flex;
  gap: 0.5rem;
  margin-bottom: 2.5rem;
  background: rgba(15, 23, 42, 0.4);
  padding: 0.5rem;
  border-radius: var(--radius-lg);
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.tab-btn {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  background: transparent;
  border: none;
  border-radius: var(--radius-md);
  color: var(--color-text-muted);
  font-weight: 500;
  cursor: pointer;
  transition: all var(--transition-base);
}

.tab-btn:hover {
  color: var(--color-text);
  background: rgba(255, 255, 255, 0.05);
}

.tab-btn.active {
  background: var(--color-primary);
  color: white;
  box-shadow: 0 4px 12px rgba(59, 130, 246, 0.4);
}

.tab-icon {
  font-size: 1.1em;
}

.topic-content {
  min-height: 50vh;
}

/* Transitions */
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from {
  transform: translateX(20px);
  opacity: 0;
}

.slide-fade-leave-to {
  transform: translateX(-20px);
  opacity: 0;
}
</style>
