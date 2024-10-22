<script lang="ts">
  let form_state = $state({
    name: 'Thayne',
    age: 30,
    email: '',
    step: 0,
    error: ''
  })

  const QUESTIONS = [
    {
      question: 'What is your name?',
      id: 'name',
      type: 'text'
    },
    {
      question: 'How old are you?',
      id: 'age',
      type: 'number'
    },
    {
      question: 'What is your email?',
      id: 'email',
      type: 'email'
    }
  ]

  const next_step = () => {
    if (form_state[QUESTIONS[form_state.step].id] === '') {
      form_state.error = 'Please fill out the form.'
      return
    }

    if (form_state.step < QUESTIONS.length - 1) {
      form_state.step += 1
      form_state.error = ''
    } else {
      form_state.error = 'You have reached the end of the form.'
    }
  }
</script>

<main>
  <p>Step: {form_state.step + 1}</p>

  <p class="text-red-700"
     class:block={form_state.error}
     class:hidden={!form_state.error}>Error: {form_state.error}</p>

  <!-- {#each QUESTIONS as question (question.id)}
    {@render form_step(question)}
  {/each} -->

  {#each QUESTIONS as {question, id, type}, index (id)}
    {#if index === form_state.step}
      {@render form_step({question, id, type})}
    {/if}
    <!-- {@render form_step({question, id, type})} -->
  {/each}

  <!-- {@render form_step({
    question: 'What is your name?',
    id: 'name',
    type: 'text'
  })} -->
</main>

{#snippet form_step({
  question,
  id,
  type
}: {
  question: string,
  id: string,
  type: string
})}
  <article>
    <div>
      <label for={id}>{question}</label>
      <input {type} {id} bind:value={form_state[id]}>
    </div>
    <button onclick={next_step}>Next</button>
  </article>
{/snippet}

<style>
  
</style>