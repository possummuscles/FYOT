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
      
      <li><a class="button" data-selected={path === '/'} href="/">Home</a></li>
      <li><a class="button" data-selected={path === '/tree'} href="/tree">Tree</a></li>
    </ul>
  </nav>
</header>

<style>

  
header {
  border: 3px solid whitesmoke;
  border-radius: 10px;
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
   
    place-content: centre;
    padding: 1rem;
}
.title {
  font-size: 2rem;
  color: #4B6E30;
  font-weight: 800;
  padding-top: 0.1rem;
  
}
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  a[data-selected='true'] {
    font-weight: 600;
    color: gray;
  }
  a {
    text-decoration: none;
    display: block;
    padding-top: 3rem;
    font-size: 2rem;
    
  }

  a:hover {
    color: #638D24
  }
    
  
.button {
        background-color: whitesmoke;
        border: 1px solid black;
        border-radius: 10px;
        color: #4B6E30;
        padding: .25rem 0.5rem;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 1rem;
        margin: 4px 2px;
        cursor: pointer;
        box-shadow: 3px 3px #888888;
}
      
  

  img {
    margin: 0;
    
    max-width: 100%;
    height: auto;
    
  }

  
  @media screen and (min-width: 400px) {
    header {
    
      align-items: center;
    }
  }
</style>
