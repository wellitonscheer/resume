<section>
  <h2 class="text-sm font-semibold uppercase tracking-widest text-gray-500 mb-1">Experience</h2>
  <div class="w-8 h-0.5 bg-blue-500 rounded mb-5"></div>

  <div class="space-y-4">
    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Full Stack Developer</h3>
      <p class="text-sm text-blue-400/80 mb-1">Setrem &mdash; Sociedade Educacional Três de Maio</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Oct 2023 – Present · ~2 yrs 5 mos</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Built internal tools and educational platforms serving students and staff across multiple Setrem systems</li>
        <li>Designed service-based architecture using RabbitMQ for async processing and Docker for deployment</li>
        <li>Created a PATCH endpoint for partial form updates — reduced payload size from ~5-10 KB to ~200-500 B and cut unnecessary DB writes by ~80%</li>
        <li>Set up and maintained Turborepo monorepo shared across multiple Next.js applications</li>
        <li>Integrated vector embeddings and semantic search into a support ticket tool (PgVector, Go)</li>
      </ul>
      <div class="flex flex-wrap gap-1.5 mt-3">
        {#each ['Go', 'TypeScript', 'Next.js', 'PostgreSQL', 'RabbitMQ', 'Docker', 'Turborepo'] as tech}
          <span class="bg-[#3a322c] text-gray-300 px-2 py-0.5 rounded text-xs">{tech}</span>
        {/each}
      </div>
    </div>

    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Software Developer</h3>
      <p class="text-sm text-blue-400/80 mb-1">A1 Lab &mdash; Freelance · Remote</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Nov 2022 – Oct 2023 · 1 yr</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Built serverless API services using Python with Lambda and CloudFormation</li>
        <li>Implemented a DynamoDB caching layer to avoid redundant third-party API calls, reducing average response time from ~1.5s to ~300ms</li>
        <li>Worked on data processing pipelines and storage solutions with DynamoDB</li>
      </ul>
      <div class="flex flex-wrap gap-1.5 mt-3">
        {#each ['Python', 'AWS Lambda', 'DynamoDB', 'CloudFormation'] as tech}
          <span class="bg-[#3a322c] text-gray-300 px-2 py-0.5 rounded text-xs">{tech}</span>
        {/each}
      </div>
    </div>

    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Software Developer (Apprentice)</h3>
      <p class="text-sm text-blue-400/80 mb-1">Setrem</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Feb 2021 – Nov 2022 · 1 yr 10 mos</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Learned the fundamentals of web development and collaborative coding</li>
        <li>Assisted with development tasks and basic programming assignments</li>
      </ul>
    </div>
  </div>
</section>
