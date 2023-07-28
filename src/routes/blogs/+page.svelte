<script>
  import Navbar from '../../contents/Navbar.svelte';
</script>

<Navbar />

<div class="flex items-center justify-center my-6">
  <div class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow-sm">
    <a href="/blogs/avyathi-fights-deepfake">
      <h2 class="mb-2 text-2xl font-bold tracking-tight text-gray-900">Avyathi fights deepfake</h2>
    </a>
    <p class="mb-3 font-normal text-gray-700">How Avyathi Fights Deepfake Threats and Ensures Online Safety?</p>

    <!-- Readmore ka button -->
    <div>
      <a
        href="/blogs/avyathi-fights-deepfake"
        class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-warmgray-900 bg-cyan-300 hover:bg-cyan-400 focus:ring-4 focus:outline-none focus:ring-cyan-200"
      >
        Read more
        <svg
          class="w-3.5 h-3.5 ml-2"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 14 10"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M1 5h12m0 0L9 1m4 4L9 9"
          />
        </svg>
      </a>
    </div>
  </div>
</div>

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.lime.50);
  }
</style>
