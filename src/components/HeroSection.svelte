<script>
  import { contact } from "../stores/stores.svelte";
  import Icon from "./../lib/Icon.svelte";
</script>

<section
  id="hero"
  class="relative flex items-center justify-center w-full min-h-screen pt-20 overflow-hidden hero-bg"
>
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <div
      class="absolute rounded-full top-1/4 left-1/4 w-96 h-96 bg-primary/10 blur-3xl animate-glow-pulse"
    ></div>
    <div
      class="absolute rounded-full bottom-1/4 right-1/4 w-80 h-80 bg-primary/5 blur-3xl animate-glow-pulse"
    ></div>
  </div>

  <div class="container relative z-10 w-full px-6 mx-auto">
    <div class="max-w-4xl text-left">
      <p class="mb-4 font-mono text-sm text-primary md:text-base">
        Hola, mi nombre es
      </p>
      <h1
        class="mb-4 text-5xl font-bold md:text-7xl lg:text-8xl text-foreground"
      >
        Ilko Arboit
      </h1>
      <h2
        class="w-full mb-8 text-3xl font-bold md:text-5xl lg:text-6xl text-muted-foreground"
      >
        Automatizo procesos y desarrollo <span class="text-gradient"
          >aplicaciones escalables</span
        >
      </h2>
      <p class="max-w-2xl mb-12 text-lg text-muted-foreground md:text-xl">
        Soy desarrollador full-stack especializado en crear aplicaciones web
        modernas, escalables y con excelente experiencia de usuario
      </p>
      <div class="flex flex-wrap items-center gap-6">
        <a
          href="#projects"
          class="px-8 py-4 font-semibold transition-all rounded-lg bg-primary text-primary-foreground hover:opacity-90 glow-effect"
          >Ver proyectos</a
        >
        <div class="flex items-center gap-4">
          <a
            href={contact.github}
            target="_blank"
            class="p-3 transition-colors border rounded-lg border-border hover:border-primary hover:text-primary"
          >
            <Icon name="GitHub" class="size-5" />
          </a>
          <a
            href={contact.linkedin}
            target="_blank"
            class="p-3 transition-colors border rounded-lg border-border hover:border-primary hover:text-primary"
          >
            <Icon name="Linkedin" class="size-5" />
          </a>
          <a
            href={contact.email}
            class="p-3 transition-colors border rounded-lg border-border hover:border-primary hover:text-primary"
          >
            <Icon name="Mail" class="size-5" />
          </a>
        </div>
      </div>
    </div>

    <div class="absolute -translate-x-1/2 bottom-12 left-1/2">
      <a
        href="#about"
        class="transition-colors text-muted-foreground hover:text-primary"
      >
        <Icon name="ArrowDown" class="size-8 animate-bounce" />
      </a>
    </div>
  </div>
</section>

<style>
  .hero-bg {
    background: radial-gradient(
      ellipse at top,
      hsl(222 47% 12%),
      hsl(222 47% 6%)
    );
  }
</style>
