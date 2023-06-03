<script lang="ts">
  export let title: string
  export let subtitle: string | undefined = undefined
</script>

<h1 class="gradient-text">{title}</h1>

{#if subtitle}
  <h3>{subtitle}</h3>
{/if}

<style>
  h1 {
    margin-top: 10%;
    margin-bottom: var(--spacing-10);
  }
</style>
