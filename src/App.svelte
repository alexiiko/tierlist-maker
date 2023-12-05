<script lang="ts">
  let count: number = 0
</script>

<button on:click={() => {count += 1 }}>Inc</button>

<h1>{count}</h1>
