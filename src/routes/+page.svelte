<script>
  import ArrowRightIcon from '$lib/components/ArrowRightIcon.svelte'
  import PostsList from '$lib/components/PostsList.svelte'
  import SocialLinks from '$lib/components/SocialLinks.svelte'
//  import Footer from '$lib/components/Footer.svelte'

  import { avatar, bio, name, slogan } from '$lib/info.js'

  /** @type {import('./$types').PageData} */
  export let data
</script>

<svelte:head>
  <title>{name}</title>
  <meta name="description" content={bio} />
</svelte:head>

<section class="flex flex-row mb-4 md:p-8 rounded-lg relativelg:-mx-40 lg:mb-44 lg:px-8 xl:-mx-54 xl:mb-[10rem] 2xl:-mx-60 2xl:mb-48 "  >
<div class="m-8 hero min-h-screen relativelg:-mx-10 lg:mb-44  xl:-mx-44 xl:mb-[10rem] 2xl:-mx-40 2xl:mb-48 " style="background-image: url(https://daisyui.com/images/stock/photo-1507358522600-9f71e620c44e.jpg);">
  <div class="hero-overlay bg-opacity-70 w-full"></div>
  <div class="hero-content text-center text-neutral-content">
    <div class="max-w-md">
      <h1 class="mb-5 text-5xl font-bold  !text-transparent bg-clip-text bg-gradient-to-r from-rose-500 to-slate-200 dark:to-slate-400">Build Letter</h1>
      <p class="mb-5 text-white">
                    {slogan}
                </p>
      <button class="btn btn-primary">Dowiedz się więcej</button>
    </div>
  </div>
</div>
    </section>
  <!-- bio -->
  <section class="flex flex-col mb-4 p-8 rounded-lg relativelg:-mx-40 lg:mb-44 lg:px-8 xl:-mx-64 xl:mb-[10rem] 2xl:-mx-60 2xl:mb-48  bg-gradient-to-r dark:from-neutral-500 dark:to-neutral-800  from-neutral-100 to-neutral-300 ">
    <div class="flex flex-col lg:flex-row items-center w-full m-2 gap-6 rounded-lg">
      <img
        src={avatar}
        alt={name}
        class="mx-auto rounded-lg md:h-72 h-48 ring-2 bg-white ring-zinc-200 dark:bg-gray-200 dark:ring-zinc-700"
      />

      <p class="prose text-base text-zinc-900 dark:text-zinc-400">
        {bio}
      </p>
    </div>
<hr class="border-0 h-px mt-8 bg-gray-600">
      <div class="mx-auto flex mt-8 gap-6">
        <SocialLinks />
      </div>
  </section>


  <section class="flex flex-col lg:flex-row mb-4 p-8 gap-8 justify-between rounded-lg relativelg:-mx-40 lg:mb-44 lg:px-8 xl:-mx-64 xl:mb-[10rem] 2xl:-mx-60 2xl:mb-48  bg-gradient-to-r dark:from-neutral-600   from-neutral-100 to-neutral-300 ">
<div class="bg-black text-white p-8 rounded-lg">Od czego zacząć? </div>
<div class="bg-black text-white p-8 rounded-lg">Jak wykonać? </div>
<div class="bg-black text-white p-8 rounded-lg">Gdzie szukać? </div>
<div class="bg-black text-white p-8 rounded-lg">Narzędzia</div>
</section>


<div class="flex flex-col flex-grow gap-8 pb-16">

  <section class="w-full">
    <div class="flex items-center justify-between gap-4 mb-8">
      <h2 class="text-sm font-medium sm:text-base text-zinc-500 dark:text-zinc-400">
        Recently Published
      </h2>
      <a href="/posts" class="flex items-center gap-1 text-sm font-medium text-teal-500"
        >View All <ArrowRightIcon class="w-4 h-4" /></a
      >
    </div>
    <PostsList posts={data.posts} />
  </section>
</div>

