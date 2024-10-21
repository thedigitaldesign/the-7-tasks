<script lang="ts">
  let count = $state(0)
  let status: 'OPEN' | 'CLOSED' = $state('OPEN')

  let increment = () => {
    count += 1
  }

  // let toggle = () => {
  //   status = status === 'OPEN' ? 'CLOSED' : 'OPEN'
  // }

  let onclick = () => {
    status = status === 'OPEN' ? 'CLOSED' : 'OPEN'
  }
</script>

<div class="min-w-7 m-auto border border-slate-800 rounded-md p-4">
  <button class="visitor" onclick={increment}>Visitors: {count}</button>

  <p>
    The store is now {status}
  </p>

  <!-- <button class="status" onclick={toggle}>Toggle store status</button> -->
  
  <button class="status" {onclick}>Toggle store status</button>
</div>

<style>
  .visitor {
    font-size: 2em;
  }

  .status {
    font-size: 1.5em;
  }
</style>