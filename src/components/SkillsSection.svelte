<script lang="ts">
  const skillCategories = [
    {
      title: "Frontend",
      skills: [
        "Svelte",
        "TypeScript",
        "React",
        "React-Native",
        "Angular",
        "Tailwind CSS",
      ],
    },
    {
      title: "Backend",
      skills: ["Java", "Go", "Express", "Python", "PHP", "Ruby"],
    },
    {
      title: "Herramientas",
      skills: [
        "Git",
        "Docker",
        "n8n",
        "Postman",
        "VS Code",
        "Linux",
        "MySQL",
        "PostgreSQL",
      ],
    },
  ];
</script>

<section id="skills" class="w-full py-10 bg-secondary/10">
  <div class="container px-6 mx-auto">
    <div class="max-w-screen">
      <h2 class="flex items-center gap-4 section-title">
        <span class="font-mono text-xl text-primary"> 03. </span>
        Habilidades
        <span class="flex-1 h-px ml-4 bg-border"></span>
      </h2>
      <div class="grid gap-8 md:grid-cols-3">
        {#each skillCategories as category, i}
          <div class="p-8 rounded-lg bg-card card-hover">
            <h3 class="mb-6 text-xl font-bold text-primary">
              {category.title}
            </h3>
            <ul class="space-y-3">
              {#each category.skills as skill, j}
                <li class="flex items-center gap-3 text-muted-foreground">
                  <span class="w-2 h-2 rounded-full bg-primary"></span>
                  {skill}
                </li>
              {/each}
            </ul>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

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
