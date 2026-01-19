<script lang="ts">
  import Icon from "../lib/Icon.svelte";
  import { contact } from "../stores/stores.svelte";
</script>

<section id="contact" class="py-32">
  <div class="container px-6 mx-auto">
    <div class="max-w-2xl mx-auto text-center">
      <p class="mb-4 font-mono text-xl text-primary">04. ¿Qué sigue?</p>
      <h2 class="mb-6 text-4xl font-bold md:text-5xl text-foreground">
        ¡Hablemos!
      </h2>
      <p class="mb-12 text-lg text-muted-foreground">
        Estoy actualmente buscando nuevas oportunidades. Ya sea que tengas una
        pregunta, una propuesta de proyecto o simplemente quieras saludar, ¡mi
        bandeja de entrada está siempre abierta!
      </p>

      <a
        href={contact.email}
        class="inline-flex items-center gap-3 px-8 py-4 font-semibold transition-colors border-2 rounded-lg border-primary text-primary hover:bg-primary/10"
      >
        <Icon name="Mail" class="size-5" />
        Enviar mensaje
      </a>
    </div>
  </div>
</section>
