<script>
  import { Link } from "svelte-routing";
  import { onMount } from "svelte";
  function mobileNav() {
    var elems = document.querySelectorAll(".sidenav");
    var instances = M.Sidenav.init(elems);
  }
</script>


<nav>
  <div class="nav-wrapper">
    <a
      href="#"
      data-target="mobile-demo"
      class="sidenav-trigger"
      on:click={mobileNav}>
      <i class="material-icons">menu</i>
    </a>
    <div class="container">
      <Link to="/">
        <span class="brand-logo">Svelte ie11 i18n materialize Template</span>
      </Link>
      <ul id="nav-mobile" class="right hide-on-small-only">
        <li>
          <Link to="/">Home</Link>
        </li>
        <li>
          <Link to="/about">About</Link>
        </li>
      </ul>
    </div>
  </div>
</nav>

<ul class="sidenav" id="mobile-demo">
  <li>
    <Link to="/">Home</Link>
  </li>
  <li>
    <Link to="/about">About</Link>
  </li>
  <li>
    <a href="http://www.seanbase.com">www.seanbase.com</a>
  </li>
</ul>