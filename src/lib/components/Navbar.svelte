<script lang="ts">
  import { page } from "$app/state";
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from "flowbite-svelte";
  let activeUrl = $state(page.url.pathname);
  $effect(() => {
    activeUrl = page.url.pathname;
  });
</script>

<Navbar color="none" class="bg-stone-700">
  <NavBrand class="text-white text-2xl font-bebas-neue" href="/">
    <p>Samuel Valencia</p>
  </NavBrand>
  <NavHamburger />
  <NavUl {activeUrl}>
    <NavLi class="text-xl font-bebas-neue" href="/">Home</NavLi>
    <NavLi class="text-xl font-bebas-neue" href="/about">About</NavLi>
    <NavLi class="text-xl font-bebas-neue" href="/contact">Contact Me</NavLi>
    <NavLi class="text-xl font-bebas-neue" href="/pictures">Pictures</NavLi>
    <NavLi class="text-xl font-bebas-neue" href="/projects">Projects</NavLi>
    <NavLi class="text-xl font-bebas-neue" href="/socials">Socials</NavLi>
    <NavLi class="text-xl font-bebas-neue" href="/vatsim">VATSIM</NavLi>
  </NavUl>
</Navbar>
