<script>
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
        <span class="brand-logo">Phone to Desk</span>
      <ul id="nav-mobile" class="right hide-on-small-only">
        <li>
            <a href="http://www.seanbase.com">www.seanbase.com</a>
        </li>
        <li>
            <a href="http://www.seanbase.com">www.seanbase.com</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<ul class="sidenav" id="mobile-demo">
  <li>
      <a href="http://www.seanbase.com">www.seanbase.com</a>
  </li>
  <li>
    <a href="http://www.seanbase.com">www.seanbase.com</a>
  </li>
  <li>
    <a href="http://www.seanbase.com">www.seanbase.com</a>
  </li>
</ul>