<script setup>
import { computed, ref } from 'vue'
import Sidebar from './components/Sidebar.vue'
import TopicView from './components/TopicView.vue'
import HomeView from './components/HomeView.vue'
import { topics } from './data/topics'

// Set the default topic to the first element (which is now ID 12) or the database one (ID 25)
const selectedTopicId = ref('home')

const selectedTopic = computed(() => {
  return topics.find(t => t.id === selectedTopicId.value) || topics[0]
})

function handleTopicSelect(id) {
  selectedTopicId.value = id
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <div class="app-container">
    <Sidebar 
      :topics="topics" 
      :selected-id="selectedTopicId" 
      @select="handleTopicSelect" 
    />
    
    <main class="main-content">
      <Transition name="fade" mode="out-in">
        <HomeView v-if="selectedTopicId === 'home'" />
        <TopicView 
          v-else
          :key="selectedTopic.id" 
          :topic="selectedTopic" 
        />
      </Transition>
    </main>
  </div>
</template>

<style>
/* Page transition animations */
.fade-enter-active,
.fade-leave-active {
  transition: opacity var(--transition-base), transform var(--transition-base);
}

.fade-enter-from {
  opacity: 0;
  transform: translateY(10px);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
