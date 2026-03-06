<script>
  import { onMount } from 'svelte'

  let { slides } = $props()

  let currentIndex = $state(0)
  let isMobile = $state(false)
  let touchStartX = 0
  let touchStartY = 0

  const total = $derived(slides.length)
  const transform = $derived(
    isMobile
      ? `translateY(-${currentIndex * 100}%)`
      : `translateX(-${currentIndex * 100}%)`
  )

  function next() {
    currentIndex = (currentIndex + 1) % total
  }

  function prev() {
    currentIndex = (currentIndex - 1 + total) % total
  }

  function goTo(index) {
    currentIndex = index
  }

  function handleKeydown(e) {
    if (e.key === 'ArrowRight' || e.key === 'ArrowDown') {
      e.preventDefault()
      next()
    } else if (e.key === 'ArrowLeft' || e.key === 'ArrowUp') {
      e.preventDefault()
      prev()
    }
  }

  function handleTouchStart(e) {
    touchStartX = e.touches[0].clientX
    touchStartY = e.touches[0].clientY
  }

  function handleTouchEnd(e) {
    const dx = e.changedTouches[0].clientX - touchStartX
    const dy = e.changedTouches[0].clientY - touchStartY
    const threshold = 50

    if (isMobile) {
      if (Math.abs(dy) > threshold && Math.abs(dy) > Math.abs(dx)) {
        if (dy < 0) next()
        else prev()
      }
    } else {
      if (Math.abs(dx) > threshold && Math.abs(dx) > Math.abs(dy)) {
        if (dx < 0) next()
        else prev()
      }
    }
  }

  onMount(() => {
    const mq = window.matchMedia('(max-width: 767px)')
    isMobile = mq.matches
    const handler = (e) => (isMobile = e.matches)
    mq.addEventListener('change', handler)
    return () => mq.removeEventListener('change', handler)
  })
</script>

<svelte:window onkeydown={handleKeydown} />

<div class="flex items-center justify-center min-h-screen p-4 md:p-8">
  {#if isMobile}
    <!-- Mobile: vertical layout -->
    <div class="flex flex-col items-center gap-4 w-full max-w-2xl">
      <button
        onclick={prev}
        class="flex items-center justify-center w-11 h-11 rounded-full bg-gray-800/60 hover:bg-gray-700/80 text-gray-400 hover:text-white transition cursor-pointer"
        aria-label="Previous slide"
      >
        <i class="fas fa-chevron-up"></i>
      </button>

      <div
        role="region"
        aria-label="Resume carousel"
        class="w-full bg-gray-900 rounded-xl border border-gray-800 overflow-hidden"
        style="height: 85vh;"
        ontouchstart={handleTouchStart}
        ontouchend={handleTouchEnd}
      >
        <div
          class="flex flex-col w-full h-full transition-transform duration-400 ease-in-out"
          style="transform: {transform}"
        >
          {#each slides as Slide, i}
            <div class="w-full shrink-0 h-full overflow-y-auto slide-content px-8 py-6">
              <Slide />
            </div>
          {/each}
        </div>
      </div>

      <button
        onclick={next}
        class="flex items-center justify-center w-11 h-11 rounded-full bg-gray-800/60 hover:bg-gray-700/80 text-gray-400 hover:text-white transition cursor-pointer"
        aria-label="Next slide"
      >
        <i class="fas fa-chevron-down"></i>
      </button>

      <!-- Dots -->
      <div class="flex gap-2">
        {#each slides as _, i}
          <button
            onclick={() => goTo(i)}
            class="w-2 h-2 rounded-full transition cursor-pointer {i === currentIndex ? 'bg-white' : 'bg-gray-600 hover:bg-gray-500'}"
            aria-label="Go to slide {i + 1}"
          ></button>
        {/each}
      </div>
    </div>
  {:else}
    <!-- Desktop: horizontal layout -->
    <div class="flex items-center gap-6 w-full max-w-5xl">
      <button
        onclick={prev}
        class="flex items-center justify-center w-11 h-11 shrink-0 rounded-full bg-gray-800/60 hover:bg-gray-700/80 text-gray-400 hover:text-white transition cursor-pointer"
        aria-label="Previous slide"
      >
        <i class="fas fa-chevron-left"></i>
      </button>

      <div class="flex-1 min-w-0 flex flex-col items-center gap-4">
        <div
          role="region"
          aria-label="Resume carousel"
          class="w-full bg-gray-900 rounded-xl border border-gray-800 overflow-hidden"
          style="height: 85vh;"
          ontouchstart={handleTouchStart}
          ontouchend={handleTouchEnd}
        >
          <div
            class="flex flex-row w-full h-full transition-transform duration-400 ease-in-out"
            style="transform: {transform}"
          >
            {#each slides as Slide, i}
              <div class="w-full shrink-0 h-full overflow-y-auto slide-content px-8 py-6">
                <Slide />
              </div>
            {/each}
          </div>
        </div>

        <!-- Dots -->
        <div class="flex gap-2">
          {#each slides as _, i}
            <button
              onclick={() => goTo(i)}
              class="w-2 h-2 rounded-full transition cursor-pointer {i === currentIndex ? 'bg-white' : 'bg-gray-600 hover:bg-gray-500'}"
              aria-label="Go to slide {i + 1}"
            ></button>
          {/each}
        </div>
      </div>

      <button
        onclick={next}
        class="flex items-center justify-center w-11 h-11 shrink-0 rounded-full bg-gray-800/60 hover:bg-gray-700/80 text-gray-400 hover:text-white transition cursor-pointer"
        aria-label="Next slide"
      >
        <i class="fas fa-chevron-right"></i>
      </button>
    </div>
  {/if}
</div>
