<script>
  import Header from '$lib/Header.svelte'
  
</script>

<div class="container">
<Header blogTitle={'F.Y.O.T.'} />

<main >
  <slot />
</main>


</div>


<style>
  :global(a) {
  color: #4B6E30
    
  }
  :global(a:hover) {
    color: #638D24;
    border-bottom: none;
  }

  main {
    padding: 1rem;
    padding-bottom: 2rem;
  }
  .container{
    position: relative;
    min-height: 100%;
  }
</style>
