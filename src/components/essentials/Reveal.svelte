<script lang="ts">
  import { onMount } from 'svelte'
  import { animReveal } from '@/utils/reveal'

  onMount(() => {
    setTimeout(() => animReveal(), 100)
  })
</script>
