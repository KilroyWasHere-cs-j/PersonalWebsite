<script lang="ts">
    import { writable } from 'svelte/store';
  
    // Store to manage the visibility of the mobile menu
    const isMobileMenuOpen = writable(false);
  
    const toggleMobileMenu = () => {
        isMobileMenuOpen.update((isOpen) => !isOpen);
    };
  </script>
  
  <nav class="bg-bgNavy shadow-md sticky top-0 z-50">
    <div class="container mx-auto flex items-center justify-between bg-black shadow-purple-900 shadow-md p-4">
        <!-- Logo Section -->
         <div class="flex flex-row space-x-2">
            <div class="">
                <svg width="20px" height="20px" viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
                    <rect width="48" height="48" fill="black"/>
                    <g id="a" transform="rotate(0, 24, 24) translate(0,-10)">
                      <polyline class="c" points="32.1313 11.85 24 36.15 15.8687 11.85" stroke="#7D359C" fill="none"/>
                    </g>
                    <g id="a" transform="rotate(180, 24, 24) translate(0,-10)">
                      <polyline class="c" points="32.1313 11.85 24 36.15 15.8687 11.85" stroke="#eb4034" fill="none"/>
                    </g>
                    <g id="b"></g>
                </svg>
            </div>
              <a href="/" class="flex items-center">
                <div class="flex flex-row space-x-1">
                    <h1 class="text-purple-900 motion-opacity-in-0">Voodu</h1>
                    <h1 class="text-green-700 motion-opacity-in-0">Software</h1>
                    <h1 class="text-white motion-opacity-in-0">.</h1>
                </div>
              </a>
         </div>
        
        <!-- Hamburger Icon for Mobile -->
        <button 
            class="text-textGold md:hidden px-4 py-2 rounded focus:outline-none text-purple-900" 
            onclick={toggleMobileMenu}>
            ☰
        </button>
        
        <!-- Navigation Links for Desktop -->
        <div class="hidden md:flex space-x-4">
            {#each ['home', 'projects', 'contact'] as link}
                <button 
                    onclick={() => (window.location.href = `/${link}`)}
                    class="text-purple-900 px-4 py-2 rounded hover:bg-green-200 hover:text-black transition duration-300"
                >
                    {link.charAt(0).toUpperCase() + link.slice(1)}
                </button>
            {/each}
        </div>
    </div>
  
    <!-- Mobile Menu -->
    {#if $isMobileMenuOpen}
        <div class="md:hidden bg-bgNavy shadow-lg space-y-2 p-4">
            {#each ['home', 'projects', 'contact'] as link}
                <button 
                    onclick={() => (window.location.href = `/${link}`)}
                    class="block text-purple-900 w-full text-left px-4 py-2 rounded hover:bg-textGold hover:text-bgNavy transition duration-300"
                >
                    {link.charAt(0).toUpperCase() + link.slice(1)}
                </button>
            {/each}
        </div>
    {/if}
  </nav>
  
  <style>
  /* Adjust spacing for responsiveness */
  .container {
    max-width: 100%;
  }
  
  button {
    cursor: pointer;
  }
  </style>
  