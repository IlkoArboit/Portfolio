<script>
  import HeroSection from "./components/HeroSection.svelte";
  import Header from "./base/Header.svelte";
  import AboutSection from "./components/AboutSection.svelte";
  import ProjectsSection from "./components/ProjectsSection.svelte";
  import SkillsSection from "./components/SkillsSection.svelte";
  import ContactSection from "./components/ContactSection.svelte";
  import Footer from "./base/Footer.svelte";
</script>

<div class="min-h-screen bg-background">
  <Header />
  <main>
    <div class="flex flex-col items-center w-full">
      <HeroSection />
      <AboutSection />
      <ProjectsSection />
      <SkillsSection></SkillsSection>
      <ContactSection></ContactSection>
    </div>
  </main>
  <Footer />
</div>

<style>
</style>
