<script lang="ts">
  import Icon from "./Icon.svelte";

  export let ProjectCardProps: {
    title: string;
    description: string;
    technologies: string[];
    githubUrl?: string;
    liveUrl?: string;
    featured?: boolean;
  };
</script>

{#if ProjectCardProps.featured}
  <div class="relative grid items-center gap-4 mb-24 md:grid-cols-12">
    <div class="relative md:col-span-7">
      <div
        class="overflow-hidden rounded-lg aspect-video bg-gradient-to-br from-primary/20 to-secondary group"
      >
        <div
          class="flex items-center justify-center w-full h-full transition-colors bg-card/80 group-hover:bg-card/50"
        >
          <Icon name="Folder" class="size-5" />
        </div>
      </div>
    </div>
    <div class="relative z-10 md:col-span-5 md:text-right">
      <p class="font-mono text-sm text-primary md-2">Proyecto destacado</p>
      <h3 class="mb-4 text-2xl font-bold text-foreground">
        {ProjectCardProps.title}
      </h3>
      <div class="p-6 mb-4 rounded-lg shadow-lg bg-card md:-ml-20">
        <p class="text-muted-foreground">{ProjectCardProps.description}</p>
      </div>
      <ul
        class="flex flex-wrap gap-3 mb-4 font-mono text-sm md:justify-end text-muted-foreground"
      >
        {#each ProjectCardProps.technologies as tech}
          <li>{tech}</li>
        {/each}
      </ul>
      <div class="flex gap-4 md:justify-end">
        {#if ProjectCardProps.githubUrl}
          <a
            href={ProjectCardProps.githubUrl}
            target="_blank"
            class="transition-colors text-muted-foreground hover:text-primary"
          >
            <Icon name="GitHub" class="size-4" />
          </a>
        {/if}
        {#if ProjectCardProps.liveUrl}
          <a
            href={ProjectCardProps.liveUrl}
            target="_blank"
            class="transition-colors text-muted-foreground hover:text-primary"
          >
            <Icon name="ExternalLink" class="size-4" />
          </a>
        {/if}
      </div>
    </div>
  </div>
{:else}
  <div class="flex flex-col h-full p-6 rounded-lg bg-card card-hover">
    <div class="flex items-center justify-between mb-6 ">
      <Icon name="Folder" class="size-10 text-primary" />
      <div class="flex gap-4">
        {#if ProjectCardProps.githubUrl}
          <a
            href={ProjectCardProps.githubUrl}
            target="_blank"
            class="transition-colors text-muted-foreground hover:text-primary"
          >
            <Icon name="GitHub" class="size-5" />
          </a>
        {/if}
        {#if ProjectCardProps.liveUrl}
          <a
            href={ProjectCardProps.liveUrl}
            target="_blank"
            class="transition-colors text-muted-foreground hover:text-primary"
          >
            <Icon name="ExternalLink" class="size-5" />
          </a>
        {/if}
      </div>
    </div>
    <h3
      class="mb-3 text-xl font-bold transition-colors text-foreground hover:text-primary"
    >
      {ProjectCardProps.title}
    </h3>
    <p class="flex-grow mb-6 text-sm text-muted-foreground">
      {ProjectCardProps.description}
    </p>
    <ul class="flex flex-wrap gap-2 font-mono text-xs text-muted-foreground">
      {#each ProjectCardProps.technologies as tech}
        <li class="px-2 py-1 rounded bg-secondary">{tech}</li>
      {/each}
    </ul>
  </div>
{/if}

<style>
  .card-hover {
    @apply transition-all duration-300;
  }

  .card-hover:hover {
    @apply -translate-y-1;
    box-shadow:
      0 4px 24px hsl(0 0% 0% / 0.4),
      0 0 40px hsl(172 66% 50% / 0.3);
  }
</style>
