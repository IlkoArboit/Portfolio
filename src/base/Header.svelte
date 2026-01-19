<script lang="ts">
  import { contact } from "../stores/stores.svelte";

  const navItems = [
    { name: "Inicio", href: "#hero" },
    { name: "Sobre mí", href: "#about" },
    { name: "Proyectos", href: "#projects" },
    { name: "Skills", href: "#skills" },
  ];
</script>

<header
  class="fixed top-0 left-0 right-0 z-50 border-b bg-background backdrop-blur-md border-border"
>
  <div class="flex items-center justify-between px-6 py-4 mx-auto">
    <a href="#hero" class="text-2xl font-bold text-gradient"
      >{"<Ilko Arboit />"}</a
    >
    <ul class="items-center hidden gap-8 md:flex">
      {#each navItems as item}
        <li>
          <a href={item.href} class="text-sm font-medium nav-link"
            >{item.name}</a
          >
        </li>
      {/each}
    </ul>
    <a
      href={contact.email}
      class="hidden px-4 py-2 text-sm font-medium transition-opacity rounded-lg md:inline-flex bg-primary text-primary-foreground hover:opacity-90"
    >
      Contacto
    </a>
  </div>
</header>

<style>
  .nav-link {
    @apply text-muted-foreground hover:text-primary transition-colors duration-200;
  }
</style>
