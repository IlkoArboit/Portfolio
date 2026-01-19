<script lang="ts">
  import Icon from "../lib/Icon.svelte";

</script>

<footer class="py-8 border-t border-border">
  <div class="container px-6 mx-auto">
    <div
      class="flex flex-col items-center justify-between gap-4 md:flex-row"
    >
      <p class="font-mono text-sm text-muted-foreground">
        Diseñado y desarrollado por <span class="text-primary"
          >Ilko Arboit</span
        >
      </p>
      <div class="flex items-center gap-6">
        <a
          href="https://github.com"
          target="_blank"
          rel="noopener noreferrer"
          class="transition-colors text-muted-foreground hover:text-primary"
        >
          <Icon name="GitHub" class="size-4" />
        </a>
        <a
          href="https://linkedin.com"
          target="_blank"
          rel="noopener noreferrer"
          class="transition-colors text-muted-foreground hover:text-primary"
        >
          <Icon name="Linkedin" class="size-4" />
        </a>
        <!-- <a
          href="https://twitter.com"
          target="_blank"
          rel="noopener noreferrer"
          class="transition-colors text-muted-foreground hover:text-primary"
        >
          <Twitter size={18} />
        </a> -->
      </div>
    </div>
  </div>
</footer>
