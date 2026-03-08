<script>
  import Carousel from './lib/Carousel.svelte'
  import HeaderAbout from './lib/slides/HeaderAbout.svelte'
  import Experience from './lib/slides/Experience.svelte'
  import OpenSource from './lib/slides/OpenSource.svelte'
  import Projects from './lib/slides/Projects.svelte'
  import Education from './lib/slides/Education.svelte'
  import { backgroundBase64 } from './lib/imageFallbacks.js'

  const slides = [HeaderAbout, Experience, OpenSource, Projects, Education]

  let bgUrl = $state('/taking_photo.JPG')

  const img = new Image()
  img.src = '/taking_photo.JPG'
  img.onerror = () => { bgUrl = backgroundBase64 }
</script>

<main class="text-gray-300 min-h-screen overflow-hidden bg-cover bg-center bg-no-repeat"
      style="background-image: url('{bgUrl}');">
  <Carousel {slides} />
</main>
