<script>
  import Header from '$lib/Header.svelte'
  import Footer from '$lib/Footer.svelte'
</script>

<Header blogTitle={'F.Y.O.T.'} />

<main style="padding: 1em">
  <slot />
</main>

<Footer />

<style>
  :global(a) {
  color: #4B6E30
    
  }
  :global(a:hover) {
    color: #638D24;
    border-bottom: none;
  }
</style>
