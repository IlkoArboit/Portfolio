<script lang="ts">
  let profilePHUrl: string =
    "https://media.licdn.com/dms/image/v2/D5603AQFhb4cvgnBXcQ/profile-displayphoto-shrink_200_200/profile-displayphoto-shrink_200_200/0/1631197021367?e=1770249600&v=beta&t=ZoRv9kmYbCijbPlP5wVmhy7qgPDRCkGE97t-Gb6lNP8";
</script>

<section id="about" class="py-32 bg-secondary/10">
  <div class="container px-6 mx-auto">
    <div class="max-w-screen">
      <h2 class="flex items-center gap-4 section-title">
        <span class="font-mono text-xl text-primary"> 01. </span>
        Sobre mí
        <span class="flex-1 h-px ml-4 bg-border"></span>
      </h2>
      <div class="grid gap-12 mt-12 md:grid-cols-3">
        <div class="space-y-6 text-left md:col-span-2">
          <p class="text-lg leading-relaxed text-muted-foreground">
            Soy desarrollador de software full stack con más de tres años de
            experiencia creando aplicaciones web y móviles. Me especializo en
            backend con Golang, Python y Express, y en frontend con React,
            Svelte y React Native.
          </p>
          <p class="text-lg leading-relaxed text-muted-foreground">
            Trabajo en el diseño de soluciones escalables, APIs REST e
            integraciones entre sistemas, incluyendo automatización de procesos
            con n8n. Me enfoco en escribir código claro, mantenible y orientado
            a resolver problemas reales.
          </p>
          <p class="text-lg leading-relaxed text-muted-foreground">
            Me caracterizo por el aprendizaje continuo, el pensamiento crítico y
            el trabajo en equipo. Busco participar en proyectos desafiantes
            donde la tecnología tenga un impacto concreto y medible.
          </p>
          <p class="text-lg leading-relaxed text-muted-foreground">
            Algunas tecnologías con las que trabajo actualmente:
          </p>
          <ul class="grid grid-cols-2 gap-2 font-mono text-sm">
            {#each ["Svelte", "Go", "Java", "React", "Express", "Python", "PostgreSQL", "React-Native", "n8n"] as tech}
              <li class="flex items-center gap-2 text-muted-foreground">
                <span class="text-primary">▹</span>
                {tech}
              </li>
            {/each}
          </ul>
        </div>
        <div class="relative group">
          <div class="relative overflow-hidden rounded-lg">
            <div
              class="flex items-center justify-center rounded-lg aspect-square bg-gradient-to-br from-primary/20 to-primary/5"
            >
              <span class="flex text-6xl size-[75%]">
                <img class="rounded-sm" src={profilePHUrl} alt="👨‍💻" />
              </span>
            </div>
            <div
              class="absolute inset-0 transition-transform translate-x-4 translate-y-4 border-2 rounded-lg border-primary -z-10 group-hover:translate-x-2 group-hover:translate-y-2"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
