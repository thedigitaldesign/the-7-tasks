<script lang="ts">
  let form_state = $state({
    name: 'Thayne',
    age: 30,
    email: '',
    step: 0,
    error: ''
  })
</script>

<main>
  <p>Step: {form_state.step + 1}</p>

  <p class="text-red-700"
     class:block={form_state.error}
     class:hidden={!form_state.error}>Error: {form_state.error}</p>

  {@render form_step({
    question: 'What is your name?',
    id: 'name',
    type: 'text'
  })}
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
  </article>
{/snippet}

<style>
  
</style>