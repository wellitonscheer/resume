<script>
  import { onMount } from 'svelte'

  let { slides } = $props()

  let currentIndex = $state(0)
  let isMobile = $state(false)
  let touchStartX = 0
  let touchStartY = 0
  let touchStartScrollTop = 0
  let contentScrolledDuringTouch = false
  let slideContainer = null

  const total = $derived(slides.length)
  const transform = $derived(
    isMobile
      ? `translateY(-${currentIndex * 185}%)`
      : `translateX(-${currentIndex * 185}%)`
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
    contentScrolledDuringTouch = false
    slideContainer = e.target.closest('.slide-content')
    if (slideContainer) {
      touchStartScrollTop = slideContainer.scrollTop
    }
  }

  function handleTouchMove(e) {
    if (!isMobile || !slideContainer) return
    const dy = e.touches[0].clientY - touchStartY
    const { scrollTop, scrollHeight, clientHeight } = slideContainer
    const isScrollable = scrollHeight > clientHeight
    if (isScrollable && !((dy > 0 && scrollTop <= 0) || (dy < 0 && scrollTop + clientHeight >= scrollHeight - 1))) {
      contentScrolledDuringTouch = true
    }
  }

  function handleTouchEnd(e) {
    const dx = e.changedTouches[0].clientX - touchStartX
    const dy = e.changedTouches[0].clientY - touchStartY
    const threshold = 50

    if (isMobile) {
      if (contentScrolledDuringTouch) {
        slideContainer = null
        return
      }
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
    slideContainer = null
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

<div class="flex items-center justify-center h-dvh overflow-hidden md:min-h-screen md:overflow-visible md:p-8">
  {#if isMobile}
    <!-- Mobile: vertical layout -->
    <div class="flex flex-col items-center w-full max-w-2xl h-dvh overflow-hidden px-4 py-2">
      <div
        role="region"
        aria-label="Resume carousel"
        class="w-full flex-1 min-h-0 overflow-hidden"
        ontouchstart={handleTouchStart}
        ontouchmove={handleTouchMove}
        ontouchend={handleTouchEnd}
      >
        <div
          class="flex flex-col w-full h-full transition-transform duration-400 ease-in-out gap-y-[85%]"
          style="transform: {transform}"
        >
          {#each slides as Slide, i}
            <div class="w-full shrink-0 h-full overflow-y-auto slide-content px-8 py-6 bg-[#261f1b] rounded-xl border border-[#3a322c]">
              <Slide />
            </div>
          {/each}
        </div>
      </div>

      <!-- Dots -->
      <div class="flex gap-2 py-2">
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
        class="flex items-center justify-center w-11 h-11 shrink-0 rounded-full bg-[#3a322c]/60 hover:bg-[#4a3f37]/80 text-gray-400 hover:text-white transition cursor-pointer"
        aria-label="Previous slide"
      >
        <i class="fas fa-chevron-left"></i>
      </button>

      <div class="flex-1 min-w-0 flex flex-col items-center gap-4">
        <div
          role="region"
          aria-label="Resume carousel"
          class="w-full overflow-hidden"
          style="height: 85vh;"
          ontouchstart={handleTouchStart}
          ontouchmove={handleTouchMove}
          ontouchend={handleTouchEnd}
        >
          <div
            class="flex flex-row w-full h-full transition-transform duration-400 ease-in-out gap-x-[85%]"
            style="transform: {transform}"
          >
            {#each slides as Slide, i}
              <div class="w-full shrink-0 h-full overflow-y-auto slide-content px-8 py-6 bg-[#261f1b] rounded-xl border border-[#3a322c]">
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
        class="flex items-center justify-center w-11 h-11 shrink-0 rounded-full bg-[#3a322c]/60 hover:bg-[#4a3f37]/80 text-gray-400 hover:text-white transition cursor-pointer"
        aria-label="Next slide"
      >
        <i class="fas fa-chevron-right"></i>
      </button>
    </div>
  {/if}
</div>
