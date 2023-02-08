<script>
  import { avatar, bio, name } from '$lib/info.js'
  import SocialLinks from './SocialLinks.svelte'
  </script>

  <!-- bio -->
  <section class="flex flex-col items-center gap-16 pt-8 pb-16 bg-slate-500">
    <div class="flex flex-col items-center w-full gap-6 rounded-lg">
      <img
        src={avatar}
        alt={name}
        class="mx-auto rounded-full w-36 h-36 ring-2 ring-zinc-200 dark:ring-zinc-700"
      />
      <div class="flex gap-6">
        <SocialLinks />
      </div>
      <p class="text-base text-zinc-600 dark:text-zinc-400">
        {bio}
      </p>
    </div>
  </section>
