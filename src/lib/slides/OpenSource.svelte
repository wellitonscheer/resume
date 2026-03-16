<section>
  <h2 class="text-sm font-semibold uppercase tracking-widest text-gray-500 mb-1">Open Source</h2>
  <div class="w-8 h-0.5 bg-[var(--accent-amber-bright)] rounded mb-5"></div>

  <div class="bg-[#3a322c]/40 rounded-lg p-5 border border-[#4a3f37]/50">
    <div class="flex items-start justify-between gap-3 mb-3">
      <h3 class="text-white font-medium">spf13/pflag — Fix getFlagType error message</h3>
      <a href="https://github.com/spf13/pflag/pull/462" target="_blank"
        class="inline-flex items-center gap-1.5 shrink-0 bg-[#4a3f37]/60 text-gray-300 px-2.5 py-1 rounded-full text-xs hover:bg-[#5a4d43]/80 hover:text-white transition">
        <i class="fas fa-external-link-alt text-[0.625rem]"></i> PR #462
      </a>
    </div>
    <p class="text-sm text-gray-300 leading-relaxed">
      While using the cobra package in a Go project, I ran into a confusing error message from pflag.
      Dug into the source, found the bug: the error was referencing the wrong flag type.
      Opened a PR with the fix and it got merged.
    </p>
  </div>
</section>
