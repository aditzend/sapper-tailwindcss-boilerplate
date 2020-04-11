<script>
  import Hamburguer from "./Hamburguer.svelte";
  import NavLink from "./NavLink.svelte";
  import AccountDropdown from "@components/AccountDropdown.svelte";

  export let segment;
  let isExpanded = false;

  //   function toggleMobileMenu(event) {
  //     isExpanded = !isExpanded;
  //   }
</script>

<header
  class="bg-gray-800 sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-3">
  <div class="flex items-center justify-between px-4 py-3 sm:p-0">
    <div>
      <img class="h-8" src="mitrol_logo_white.svg" alt="Mitrol" />
    </div>
    <div class="sm:hidden">
      <button
        on:click={e => (isExpanded = !isExpanded)}
        type="button"
        class="block md:hidden text-gray-500 focus:text-white hover:text-white">
        <svg
          class="h-6 w-6 fill-current"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24">
          <path
            class={!isExpanded && 'hidden'}
            d="M16.24 14.83a1 1 0 0 1-1.41 1.41L12 13.41l-2.83 2.83a1 1 0 0
            1-1.41-1.41L10.59 12 7.76 9.17a1 1 0 0 1 1.41-1.41L12
            10.59l2.83-2.83a1 1 0 0 1 1.41 1.41L13.41 12l2.83 2.83z" />

          <path
            class={isExpanded && 'hidden'}
            d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1
            0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z" />
        </svg>
      </button>
    </div>
  </div>
  <nav class="{!isExpanded && 'hidden'} px-2 pt-2 pb-4 sm:flex sm:p-0">
    <a
      href="https://faia.org"
      class="block text-white font-semibold rounded px-2 py-1 hover:bg-gray-800">
      Nano Cursos
    </a>
    <a
      href="https://faia.org"
      class="mt-1 block text-white font-semibold rounded px-2 py-1
      hover:bg-gray-800 sm:mt-0 sm:ml-2">
      Nano Certificados
    </a>
    <a
      href="https://faia.org"
      class="mt-1 block text-white font-semibold rounded px-2 py-1
      hover:bg-gray-800 sm:mt-0 sm:ml-2">
      Perfil
    </a>
    <div class="ml-6">
      <AccountDropdown />
    </div>
  </nav>
</header>
<!-- <div>
  <div class="sm:hidden md:block flex items-center px-4 pt-2 pb-4 ">
    <a
      href="https://faia.org"
      class="block text-white font-semibold rounded px-2 py-1 hover:bg-gray-800">
      Nano Cursos
    </a>
    <a
      href="https://faia.org"
      class="mt-1 block text-white font-semibold rounded px-2 py-1
      hover:bg-gray-800">
      Nano Certificados
    </a>
    <a
      href="https://faia.org"
      class="mt-1 block text-white font-semibold rounded px-2 py-1
      hover:bg-gray-800">
      Perfil
    </a>
    <AccountDropdown />
  </div>

</div> -->
