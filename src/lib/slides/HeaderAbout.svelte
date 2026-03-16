<script>
  import { profilePhotoBase64 } from '../imageFallbacks.js'

  let photoSrc = $state('/me_center.jpg')

  function handleImgError() {
    photoSrc = profilePhotoBase64
  }
</script>

<div>
  <!-- Top row: name+pills left, photo right -->
  <div class="flex flex-col md:flex-row items-center md:items-start gap-8">
    <div class="shrink-0 md:order-last">
      <img src={photoSrc} alt="Welliton Scheer"
           onerror={handleImgError}
           class="w-44 h-44 md:w-52 md:h-52 rounded-full object-cover border-2 border-[#4a3f37]" />
    </div>
    <div class="flex-1 min-w-0">
      <header class="text-center md:text-left">
        <h1 class="text-3xl font-bold text-white mb-1">Welliton Scheer</h1>
        <p class="text-lg text-gray-400 mb-4">Full-Stack Software Developer</p>
        <div class="flex flex-col gap-2 text-sm">
          <div class="flex flex-wrap justify-center md:justify-start gap-2.5">
            <span class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full">
              <i class="fas fa-map-marker-alt text-xs"></i>Três de Maio, RS, Brazil
            </span>
            <a href="mailto:wellitonscheer@gmail.com" class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full hover:bg-[#4a3f37]/80 hover:text-white transition">
              <i class="fas fa-envelope text-xs"></i>Email
            </a>
            <a href="https://github.com/wellitonscheer" target="_blank" class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full hover:bg-[#4a3f37]/80 hover:text-white transition">
              <i class="fab fa-github text-xs"></i>GitHub
            </a>
            <a href="https://linkedin.com/in/welliton-scheer" target="_blank" class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full hover:bg-[#4a3f37]/80 hover:text-white transition">
              <i class="fab fa-linkedin text-xs"></i>LinkedIn
            </a>
          </div>
          <div class="flex flex-wrap justify-center md:justify-start gap-2.5">
            <span class="inline-flex items-center gap-1.5 bg-[var(--accent-sage-10)] text-[var(--accent-sage)] px-3 py-1 rounded-full">
              <i class="fas fa-globe text-xs"></i>Open to remote work (independent contractor)
            </span>
            <span class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full">
              <i class="fas fa-language text-xs"></i>PT (native) / EN (professional working)
            </span>
          </div>
        </div>
      </header>
    </div>
  </div>

  <!-- Divider (full width) -->
  <div class="w-12 h-px bg-[#4a3f37] mx-auto md:mx-0 my-6"></div>

  <!-- About (full width below) -->
  <section>
    <h2 class="text-sm font-semibold uppercase tracking-widest text-gray-500 mb-1">About</h2>
    <div class="w-8 h-0.5 bg-[var(--accent-amber-bright)] rounded mb-4"></div>
    <p class="text-gray-300 leading-relaxed text-[0.9375rem]">
      Full-stack developer focused on building tools that replace manual processes and save time.
      At Setrem, I built platforms used by ~1,000 people: an event system that moved evaluations
      from paper to digital, an AI report writer for professors, and an online enrollment portal.
      I work mostly with Go and TypeScript on backend services, with experience in
      microservices, message queues, PostgreSQL, Docker, and AI integration (vector search, RAG, Claude API).
      I also found and fixed a bug in an open source library I use.
      Currently studying Database Technology with a focus on Data Analytics.
    </p>
  </section>
</div>
