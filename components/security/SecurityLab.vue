<template>
  <div class="security-lab">
    <h2 class="lab-title">Laboratoire de Sécurité Interactive</h2>
    <p class="lab-description">
      Testez vos connaissances avec ces exercices pratiques basés sur des scénarios réels
    </p>

    <div class="exercise-container">
      <div 
        v-for="(exercise, index) in exercises"
        :key="exercise.id"
        class="exercise-card"
        :class="{ 'active': activeExercise === index }"
      >
        <div class="exercise-header" @click="toggleExercise(index)">
          <h3>Exercice {{ index + 1 }}: {{ exercise.title }}</h3>
          <span class="difficulty" :class="exercise.difficulty">
            {{ exercise.difficulty }}
          </span>
        </div>

        <div v-if="activeExercise === index" class="exercise-content">
          <div class="scenario">
            <h4>Scénario :</h4>
            <p>{{ exercise.scenario }}</p>
          </div>

          <div class="challenge">
            <h4>Défi :</h4>
            <p>{{ exercise.challenge }}</p>
            <div v-if="exercise.codePrompt" class="code-editor">
              <MonacoEditor
                v-model="exercise.userCode"
                :language="exercise.language"
                :options="editorOptions"
              />
            </div>
          </div>

          <div class="actions">
            <button @click="checkSolution(index)" class="check-button">
              Vérifier la solution
            </button>
            <button @click="showSolution(index)" class="solution-button">
              Voir la solution
            </button>
          </div>

          <div v-if="exercise.showFeedback" class="feedback" :class="exercise.isCorrect ? 'correct' : 'incorrect'">
            {{ exercise.feedback }}
          </div>

          <div v-if="exercise.showSolution" class="solution">
            <h4>Solution :</h4>
            <pre><code>{{ exercise.solution }}</code></pre>
            <p class="explanation">{{ exercise.explanation }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  exercises: {
    type: Array,
    required: true,
    default: () => []
  }
})

const activeExercise = ref(null)
const editorOptions = ref({
  fontSize: 14,
  minimap: { enabled: false },
  lineNumbers: 'on'
})

const toggleExercise = (index) => {
  activeExercise.value = activeExercise.value === index ? null : index
}

const checkSolution = (index) => {
  // Logique de vérification
}

const showSolution = (index) => {
  // Afficher la solution
}
</script>

<style scoped>
.security-lab {
  background-color: #f8fafc;
  border-radius: 0.5rem;
  padding: 1.5rem;
  margin: 2rem 0;
}

.lab-title {
  font-size: 1.5rem;
  font-weight: 600;
  color: #1e293b;
  margin-bottom: 0.5rem;
}

.lab-description {
  color: #64748b;
  margin-bottom: 1.5rem;
}

.exercise-card {
  border: 1px solid #e2e8f0;
  border-radius: 0.375rem;
  margin-bottom: 1rem;
  overflow: hidden;
}

.exercise-header {
  background-color: #ffffff;
  padding: 1rem;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.exercise-header h3 {
  font-size: 1.125rem;
  font-weight: 500;
  color: #1e293b;
}

.difficulty {
  padding: 0.25rem 0.5rem;
  border-radius: 0.25rem;
  font-size: 0.875rem;
  font-weight: 500;
}

.beginner {
  background-color: #ecfdf5;
  color: #059669;
}

.intermediate {
  background-color: #fef3c7;
  color: #d97706;
}

.advanced {
  background-color: #fee2e2;
  color: #dc2626;
}

.exercise-content {
  padding: 1rem;
  background-color: #f1f5f9;
}

.exercise-content > div {
  margin-bottom: 1rem;
}

.code-editor {
  height: 200px;
  border: 1px solid #cbd5e1;
  border-radius: 0.25rem;
  margin-top: 0.5rem;
}

.actions {
  display: flex;
  gap: 0.5rem;
}

button {
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
  font-weight: 500;
  cursor: pointer;
}

.check-button {
  background-color: #3b82f6;
  color: white;
  border: none;
}

.solution-button {
  background-color: white;
  color: #3b82f6;
  border: 1px solid #3b82f6;
}

.feedback {
  padding: 1rem;
  border-radius: 0.25rem;
  font-weight: 500;
}

.correct {
  background-color: #ecfdf5;
  color: #059669;
}

.incorrect {
  background-color: #fee2e2;
  color: #dc2626;
}

.solution pre {
  background-color: #1e293b;
  color: #f8fafc;
  padding: 0.75rem;
  border-radius: 0.375rem;
  overflow-x: auto;
}

.explanation {
  margin-top: 0.5rem;
  color: #475569;
}
</style>
