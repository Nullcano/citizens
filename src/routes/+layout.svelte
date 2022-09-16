<script>
	import '../styles/upmark.css';
	import '../styles/fonts.css';
	import '../styles/global.css';
  import AppHeader from '../lib/AppHeader.svelte';
</script>

<main>
  <AppHeader />
  <slot />
</main>

<style>
  main {
    margin: 0 auto;
    max-width: 60rem;
    width: 100%;
  }
</style>