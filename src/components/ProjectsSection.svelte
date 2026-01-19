<script lang="ts">
  import ProjectCard from "../lib/ProjectCard.svelte";

  let featuredProjects = [
    {
      title: "Portfolio personal",
      description:
        "Sitio web personal para mostrar proyectos y experiencia profesional.",
      technologies: ["SvelteKit", "Tailwind", "Github Pages"],
      githubUrl: "https://github.com/IlkoArboit/Portfolio",
      liveUrl: "https://ilkoarboit.github.io/Portfolio/",
      featured: true,
    },
  ];
  let otherProjects = [];
</script>

<section id="projects" class="w-full py-10">
  <div class="container px-6 mx-auto">
    <div>
      <h2 class="flex items-center gap-4 mb-16 section-title">
        <span class="font-mono text-xl text-primary"> 02. </span>
        Proyectos
        <span class="flex-1 h-px ml-4 bg-border"></span>
      </h2>

      <!-- Proyectos destacados -->
      <div class="mb-20 ">
        {#each featuredProjects as project, i}
          <div
            class={`${i % 2 === 1 ? "md:[direction:rtl] md:[&>*]:text-left md:[&>*]:[direction:ltr]" : ""}`}
          >
            <ProjectCard ProjectCardProps={project} />
          </div>
        {/each}
      </div>
      {#if otherProjects.length !== 0}
        <h3 class="mb-12 text-2xl font-bold text-center text-foreground">
          Otros proyectos destacados
        </h3>
        <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
          {#each otherProjects as project, i}
            <ProjectCard ProjectCardProps={project} />
          {/each}
        </div>
      {/if}
    </div>
  </div>
</section>
