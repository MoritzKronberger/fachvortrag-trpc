<script lang="ts">
  import { browser } from '$app/environment'
  import { goto } from '$app/navigation'
  import type { PageData } from '../../../.svelte-kit/types/src/routes/[slide]/$types'
  import Cover from './slides/cover.svelte'
  import Error from './slides/error.svelte'
  import Intro1 from './slides/intro1.svelte'
  import Intro2 from './slides/intro2.svelte'
  import './style.css'

  export let data: PageData

  const slides = [Cover, Intro1, Intro2]

  const fallbackSlide = Error

  let slide = data.slide

  // Keep slide index in bounds
  $: if (slide > slides.length - 1) slide = 0
  $: if (slide < 0) slide = slides.length - 1

  // Navigate on slide update
  $: if (browser) goto(slide.toString())

  /** Update slide index on right-/ left-arrow press. */
  const handleKeydown = (e: KeyboardEvent) => {
    const { key } = e
    console.log(key)
    if (key === 'ArrowRight') {
      slide++
    } else if (key === 'ArrowLeft') {
      slide--
    }
  }
</script>

<!-- Capture key events -->
<svelte:window on:keydown={handleKeydown} />

<!-- Display slide based on page parameter -->
<svelte:component this={slides[data.slide] ?? fallbackSlide} />
