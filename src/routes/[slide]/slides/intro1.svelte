<script lang="ts">
  import ContentSlide from '../components/ContentSlide.svelte'
  import List from '../components/List.svelte'
</script>

<ContentSlide title="Intro 2" columns={2}>
  <svelte:fragment slot="c1">
    <List>
      <li>Some very interesting</li>
      <li>unordered list</li>
      <li>bullet points</li>
    </List>
  </svelte:fragment>
  <svelte:fragment slot="c2">
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Facilis fugit sequi quos sed earum. Nihil facere alias
    pariatur amet quidem? Nisi at praesentium veniam laboriosam beatae dolorum quis facere odit?
  </svelte:fragment>
</ContentSlide>
