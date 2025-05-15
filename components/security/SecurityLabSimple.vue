<template>
  <div class="security-lab">
    <h2 class="text-2xl font-bold mb-4">Laboratoire de Sécurité</h2>
    
    <div v-for="(exercise, index) in exercises" :key="index" class="mb-8">
      <div class="exercise-card p-4 border rounded-lg">
        <h3 class="text-xl font-semibold">{{ exercise.title }}</h3>
        <p class="my-2 text-gray-600">{{ exercise.description }}</p>
        
        <div class="my-4">
          <h4 class="font-medium mb-2">Votre solution :</h4>
          <textarea
            v-model="exercise.userCode"
            class="w-full h-40 p-2 font-mono text-sm bg-gray-800 text-white rounded"
            :placeholder="'Entrez votre code ' + exercise.language"
          ></textarea>
        </div>
        
        <button 
          @click="checkSolution(index)"
          class="px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 transition"
        >
          Vérifier
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const exercises = [
  {
    title: "Prévention des injections SQL",
    description: "Implémentez une requête paramétrée pour sécuriser ce code.",
    language: "SQL",
    solution: "SELECT * FROM users WHERE username = ? AND password = ?",
    userCode: ""
  },
  {
    title: "Validation des entrées",
    description: "Créez une validation pour les données utilisateur.",
    language: "JavaScript", 
    solution: "function validate(input) {\n  // Votre code ici\n}",
    userCode: ""
  }
]

const checkSolution = (index) => {
  const exercise = exercises[index]
  if (exercise.userCode.trim() === exercise.solution.trim()) {
    alert("✅ Solution correcte!")
  } else {
    alert("⚠️ Solution incorrecte, essayez encore")
  }
}
</script>
