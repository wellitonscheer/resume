<section>
  <h2 class="text-sm font-semibold uppercase tracking-widest text-gray-500 mb-1">Experience</h2>
  <div class="w-8 h-0.5 bg-[var(--accent-amber-bright)] rounded mb-5"></div>

  <div class="space-y-4">
    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Full Stack Developer</h3>
      <p class="text-sm text-[var(--accent-teal-80)] mb-1">Setrem &mdash; Sociedade Educacional Três de Maio</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Oct 2023 – Present · ~2 yrs 5 mos</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Built an event management platform for ~1,000 users that replaced paper-based evaluations. Containerized with Docker and deployed with RabbitMQ for queue-based email delivery</li>
        <li>Found a form-save flow that deleted and reinserted entire records on every save. Replaced it with partial PATCH updates: ~95% smaller payloads, ~80% fewer DB writes</li>
        <li>Added semantic search to a support ticket system with vector embeddings (PgVector, Go). Users describe problems in plain language instead of guessing exact keywords</li>
        <li>Automated educational report writing with n8n and Claude AI. Professors email evaluation notes and receive formatted reports, replacing a manual process that cost hundreds of hours per semester</li>
      </ul>
      <div class="flex flex-wrap gap-1.5 mt-3">
        {#each ['Go', 'TypeScript', 'Next.js', 'PostgreSQL', 'RabbitMQ', 'Docker', 'n8n', 'PgVector'] as tech}
          <span class="bg-[#3a322c] text-gray-300 px-2 py-0.5 rounded text-xs">{tech}</span>
        {/each}
      </div>
    </div>

    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Software Developer</h3>
      <p class="text-sm text-[var(--accent-teal-80)] mb-1">A1 Lab &mdash; Freelance · Remote</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Nov 2022 – Oct 2023 · 1 yr</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Built serverless API services for a gym platform. Handled nearest-gym matching and randomized user locations to protect privacy</li>
        <li>Implemented a DynamoDB caching layer that cut API response time from ~1.5s to ~300ms by removing redundant third-party calls</li>
      </ul>
      <div class="flex flex-wrap gap-1.5 mt-3">
        {#each ['Python', 'AWS Lambda', 'DynamoDB', 'CloudFormation'] as tech}
          <span class="bg-[#3a322c] text-gray-300 px-2 py-0.5 rounded text-xs">{tech}</span>
        {/each}
      </div>
    </div>

    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Software Developer (Apprentice)</h3>
      <p class="text-sm text-[var(--accent-teal-80)] mb-1">Setrem</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Feb 2021 – Nov 2022 · 1 yr 10 mos</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Learned the fundamentals of web development and collaborative coding</li>
        <li>Assisted with development tasks and basic programming assignments</li>
      </ul>
    </div>
  </div>
</section>
