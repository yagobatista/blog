<script lang="typescript">
  export let segment
</script>

<style>
  nav {
    border-bottom: 1px solid rgba(255, 62, 0, 0.1);
    font-weight: 300;
    padding: 0 1em;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  /* clearfix */
  ul::after {
    content: '';
    display: block;
    clear: both;
  }

  li {
    display: block;
    float: left;
  }

  [aria-current] {
    position: relative;
    display: inline-block;
  }

  [aria-current]::after {
    position: absolute;
    content: '';
    width: calc(100% - 2em);
    height: 2px;
    background-color: lightskyblue;
    display: block;
    bottom: -1px;
  }

  a {
    text-decoration: none;
    padding: 1em;
    display: block;
  }

  .hide {
    display: none;
  }
</style>

<nav class="top-menu">
  <ul>
    <li>
      <a aria-current={segment === undefined ? 'page' : undefined} href=".">🏡Home</a>
    </li>

    <li>
      <a rel="prefetch" aria-current={segment === 'blog' ? 'page' : undefined} href="blog">
        Coding Blog
      </a>
    </li>

    <li>
      <a rel="prefetch" aria-current={segment === 'ts' ? 'page' : undefined} href="ts">TS Tips</a>
    </li>

    <li>
      <a href="feed.xml" class="hide">Feed</a>
    </li>
  </ul>
</nav>
