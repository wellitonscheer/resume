<section>
  <h2 class="text-sm font-semibold uppercase tracking-widest text-gray-500 mb-1">Experience</h2>
  <div class="w-8 h-0.5 bg-[var(--accent-amber-bright)] rounded mb-5"></div>

  <div class="space-y-4">
    <div class="bg-[#3a322c]/40 rounded-lg p-4">
      <h3 class="text-white font-medium">Full Stack Developer</h3>
      <p class="text-sm text-[var(--accent-teal-80)] mb-1">Setrem &mdash; Sociedade Educacional Três de Maio</p>
      <span class="inline-block text-xs text-gray-400 bg-[#4a3f37]/50 px-2 py-0.5 rounded mb-3">Oct 2023 – Present · ~2 yrs 5 mos</span>
      <ul class="list-disc list-inside space-y-1 text-sm text-gray-300 marker:text-gray-600">
        <li>Built an event management platform for ~1,000 users, replacing a paper-based evaluation process — professors now score projects digitally, eliminating manual data migration and accelerating result delivery</li>
        <li>Built an online enrollment system that replaced in-person document submission — staff review, request changes, and process enrollments entirely online, connected to the school's primary system for subject selection</li>
        <li>Designed queue-based email delivery with RabbitMQ ensuring zero lost notifications, and containerized all services with Docker for rapid failure recovery and one-command redeployment</li>
        <li>Replaced a delete-and-reinsert form-save pattern with partial PATCH updates — reduced payload by ~95%, cut unnecessary DB writes by ~80%, and eliminated data inconsistency risks</li>
        <li>Integrated semantic search into a support ticket system using vector embeddings (PgVector, Go) — replaced a slow, content-blind manual search with natural-language queries that find relevant tickets without exact keywords</li>
        <li>Automated educational report writing with n8n and AI — professors send evaluation notes via email and receive properly formatted reports, replacing a paid manual process and saving hundreds of hours per class</li>
        <li>Migrated 40+ repositories from self-hosted Gitea to GitHub with a custom Bash script, decommissioning an internal server and freeing infrastructure resources</li>
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
        <li>Built serverless API services for a gym platform — handled nearest-gym matching and privacy-preserving location randomization for user safety</li>
        <li>Implemented a DynamoDB caching layer that cut API response time from ~1.5s to ~300ms by eliminating redundant third-party calls</li>
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
