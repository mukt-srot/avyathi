<script>
  let isMenuOpen = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }
</script>

<nav class="sticky top-0 z-50 bg-lime-50">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
  <a href="/" class="flex items-center">
      <img src="https://svgshare.com/i/voq.svg" class="h-12 mr-3" alt="Avyathi-logo"/>
  </a>
  <div class="flex md:order-2">

      <button type="button" class="text-warmGray-900 bg-cyan-100 hover:bg-cyan-400 focus:ring-4 focus:outline-none focus:ring-cyan-200 font-medium rounded-lg text-md px-4 py-2 text-center mr-3 md:mr-0"><a href="https://github.com/mukt-srot/avyathi" target="_blank">Github</a></button>
      <button
      data-collapse-toggle="navbar-cta"
      type="button"
      class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200"
      aria-controls="navbar-cta"
      aria-expanded="{isMenuOpen}"
      on:click={toggleMenu}
    >
      <span class="sr-only">Open main menu</span>
      <svg
        class="w-5 h-5"
        aria-hidden="true"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 17 14"
      >
        <path
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M1 1h15M1 7h15M1 13h15"
        />
      </svg>
    </button>
  </div>
    <div
    class="items-center justify-between w-full md:flex md:w-auto md:order-1"
    id="navbar-cta"
    class:hidden={!isMenuOpen}
  >
    <ul class="flex flex-col font-medium p-4 md:p-0 mt-4 border rounded-lg md:flex-row md:space-x-8 md:mt-0 md:border-0">
      <li>
        <a
          href="/"
          class="block py-2 pl-3 pr-4 text-gray-900 rounded md:bg-transparent md:hover:text-lime-600 md:p-0 "
        >
          Home
        </a>
      </li>
      <li>
        <a
          href="/blogs"
          class="block py-2 pl-3 pr-4 text-gray-900 rounded  md:hover:bg-transparent md:hover:text-lime-600 md:p-0 "
        >
          Blogs
        </a>
      </li>
      <li>
        <a
          href="/privacy-policy"
          class="block py-2 pl-3 pr-4 text-gray-900 rounded  md:hover:bg-transparent md:hover:text-lime-600 md:p-0"
        >
          Privacy Policy
        </a>
      </li>
      <li>
        <a
          href="/about-us"
          class="block py-2 pl-3 pr-4 text-gray-900 rounded  md:hover:bg-transparent md:hover:text-lime-600 md:p-0"
        >
          About Us
        </a>
      </li>
    </ul>
  </div>
</div>
  
</nav>
