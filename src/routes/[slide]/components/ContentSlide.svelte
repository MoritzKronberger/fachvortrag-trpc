<script lang="ts">
  export let title: string
  export let columns: 1 | 2 | 3 = 2
</script>

<h2>{title}</h2>

<div class="content">
  {#if columns === 1}
    <div class="column"><slot name="c1" /></div>
  {:else if columns === 2}
    <div class="column"><slot name="c1" /></div>
    <div class="column"><slot name="c2" /></div>
  {:else if columns === 3}
    <div class="column"><slot name="c1" /></div>
    <div class="column"><slot name="c2" /></div>
    <div class="column"><slot name="c3" /></div>
  {/if}
</div>

<style>
  h2 {
    margin-bottom: var(--spacing-10);
  }

  .content {
    width: 100%;
    display: flex;
    gap: var(--spacing-10);
  }

  .column {
    width: 100%;
  }
</style>
