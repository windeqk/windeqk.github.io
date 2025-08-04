<script lang="ts">
  import '../app.css';
  let { children } = $props();

  const navbarLinks = [
    {
      href: '/posts',
      label: 'Posts',
    },
  ];
</script>

<div class="flex flex-col items-center gap-8">
  <navbar class="mx-auto flex w-full max-w-[700px] flex-row items-center justify-between gap-2 p-4">
    <div
      class="flex flex-row items-center gap-4 rounded-2xl bg-[rgb(var(--m3-scheme-primary-container))] p-2"
    >
      <img src="https://github.com/windeqk.png" alt="windeqk" class="size-8 rounded-full" />
      <h1 class="text-2xl font-bold tracking-wider">Windeqk's blog</h1>
    </div>
    <ul>
      {#each navbarLinks as link}
        <li><a href={link.href}>{link.label}</a></li>
      {/each}
    </ul>
  </navbar>

  <main class="mx-auto min-h-[calc(100vh-12.5rem)] w-full max-w-[700px]">
    {@render children()}
  </main>

  <footer class="p-4">
    <span class="text-[rgb(var(--m3-scheme-inverse-on-surface))]"
      >&copy; 2025
      <a href="https://windeqk.github.io">Windeqk's blog</a></span
    >
  </footer>
</div>
