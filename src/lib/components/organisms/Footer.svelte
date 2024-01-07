<!-- Footer.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte'; 
</script>

<footer>
  <hr>
  <nav>
    <ul>
      <li> 
        <a href="/rss">
          <Icon name='rss' width='1rem' height='1.5rem'/>
        </a>
      </li>
      <li> 
        <a href="/github">
          <Icon name='github' width='1rem' height='1.5rem'/>
        </a>
      </li>
      <li> 
        <a href="/">
          <Icon name='home' width='1rem' height='1.5rem'/>
        </a>
      </li>
    </ul>
  </nav>
  <p>made with sveltekit</p>
</footer>

<!-- Component Styling -->
<style>
  footer {
    margin: 0;
    padding-top: 0;
    background: #fffff5;
    display: block;
    /* flex-wrap: wrap; */
    justify-content: space-between;
    font-size: 1rem;
    line-height: 1.5rem;
  }

  hr {
    border: 0;
    border-bottom: thin solid #ccc;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    gap: 1rem;
  }

  a {
    text-decoration: none;
    color: #000; 
  }

  p {
    margin: 0;
    padding: 0;
    color: #000;
    display: flex;
    flex-wrap: wrap;
  }
</style>
