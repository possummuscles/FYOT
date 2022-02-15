<script context="module">
  import {page} from '$app/stores'
</script>

<script>
  export let blogTitle = 'My Blog'

  let path
  $: ({path} = $page)
</script>

<header>
  <img src="/FYOT_Logo.png" alt="FYTO Logo">
  <span class="title"   >{blogTitle}</span>
  
  <nav>
    <ul>
      <li><a data-selected={path === '/'} href="/">Home</a></li>
    </ul>
  </nav>
</header>

<style>

.title {
  font-size: 3rem;
  color: #4B6E30;
  font-weight: 800;
  padding-top: 2rem;
  
}
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  a[data-selected='true'] {
    font-weight: 600;
    color: #638D24;
  }
  a {
    text-decoration: none;
    display: block;
    padding-top: 3rem;
    font-size: 1rem;
  }

  header {
    display: flex;
    flex-direction: row-reverse;
    justify-content: space-around;
    align-items: flex-start;
    padding: 1em;
  }

  img {
    margin: 0;
    
    max-width: 30%;
    height: auto;
  }

  .title {
    
  }
  @media screen and (min-width: 400px) {
    header {
    
      align-items: center;
    }
  }
</style>
