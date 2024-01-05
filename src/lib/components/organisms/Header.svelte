<!-- Header.svelte -->
<header>
  <nav>
    <ul>
      <li>
        <a href="/">david han</a>
      </li>
      <li>
        <span>|</span>
      </li>
      <li>
        <a href="/blog">blog</a>
      </li>
      <li>
        <a href="/about">about</a>
      </li>
      <li>
        <a href="/contact">contact</a>
      </li>
    </ul>
  </nav>
</header>

<!-- Component Styling -->
<style>

  header {
    margin: 0;
    padding-top: 2rem;
    padding-right: 0;
    padding-bottom: 1rem;
    padding-left: 0;
    background: #fffff5;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;   
    align-content: start;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    gap: 1rem;
  }

  ul li:first-child {
    font-weight: bold;
    color: #ccc;
  }

  a {
    text-decoration: none;
    color: #000; 
  }

  a:hover {
    text-decoration: underline;
  }
</style>
