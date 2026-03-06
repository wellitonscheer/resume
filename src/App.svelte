<script>
  import Carousel from './lib/Carousel.svelte'
  import HeaderAbout from './lib/slides/HeaderAbout.svelte'
  import Experience from './lib/slides/Experience.svelte'
  import OpenSource from './lib/slides/OpenSource.svelte'
  import Projects from './lib/slides/Projects.svelte'
  import Education from './lib/slides/Education.svelte'

  const slides = [HeaderAbout, Experience, OpenSource, Projects, Education]
</script>

<main class="text-gray-300 min-h-screen overflow-hidden bg-cover bg-center bg-no-repeat"
      style="background-image: url('/taking_photo.JPG');">
  <Carousel {slides} />
</main>
