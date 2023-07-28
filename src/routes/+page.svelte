<script>
  import Forms from '../contents/Forms.svelte';
  import Navbar from '../contents/Navbar.svelte';
</script>

<main>
  <div>
    <Navbar />
  </div>
  <Forms />
</main>

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.lime.50);
  }
</style>
