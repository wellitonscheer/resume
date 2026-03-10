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
        <div class="flex flex-wrap justify-center md:justify-start gap-2.5 text-sm">
          <span class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full">
            <i class="fas fa-map-marker-alt text-xs"></i>RS, Brazil
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
          <span class="inline-flex items-center gap-1.5 bg-[#3a322c]/60 text-gray-300 px-3 py-1 rounded-full">
            <i class="fas fa-language text-xs"></i>PT (native) / EN (intermediate)
          </span>
        </div>
      </header>
    </div>
  </div>

  <!-- Divider (full width) -->
  <div class="w-12 h-px bg-[#4a3f37] mx-auto md:mx-0 my-6"></div>

  <!-- About (full width below) -->
  <section>
    <h2 class="text-sm font-semibold uppercase tracking-widest text-gray-500 mb-1">About</h2>
    <div class="w-8 h-0.5 bg-blue-500 rounded mb-4"></div>
    <p class="text-gray-300 leading-relaxed text-[0.9375rem]">
      Full-stack developer focused on building tools that replace manual processes and save time.
      At Setrem, I built platforms used by ~1,000 people — digitizing paper-based evaluations,
      automating report writing with AI, and enabling online enrollment.
      I work mostly with Go and TypeScript on backend services, and have experience with
      microservices, message queues, PostgreSQL, Docker, and AI integration (vector search, RAG, Claude API).
      When I hit a bug in a library I was using, I dug into the source code and contributed a fix upstream.
      Currently studying Database Technology with a focus on Data Analytics.
    </p>
  </section>
</div>
