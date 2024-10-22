<script lang="ts">
  let form_state = $state({
    name: 'Thayne',
    age: 30,
    email: '',
    step: 0,
    error: ''
  })

  // Debugging rune
  $inspect(form_state.step)

  // Will run onMount
  $effect(() => {
    console.log('>> on mounted')

    return () => {
      // When unmounted or destroyed will run this
      // Before the effect re-runs
      console.log('>> on unmounted')
    }
  })

  // Runs when something changes
  $effect(() => {
    // This will run every time form_state.step changes
    console.log('>> form_state.step changed', form_state.step)

    // DON'T create state inside an effect
    // Use $derived instead

    return () => {
      console.log('>> on unmounted 2')
    }
  })
</script>

<div>
  
</div>

<style>
  
</style>