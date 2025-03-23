<script>
  import TopHeader from "./components/TopHeader.svelte";
  import RetroComponent from "./01-03.svelte";
  import ForbiddenComponent from "./19.svelte";
  import NotFoundComponent from "./20.svelte";
  import IframeComponent from "./24-26.svelte";

  let selectedYear = "2001-2003";

  function selectYear(year) {
    if (selectedYear !== year) {
      selectedYear = year;
    }
  }
</script>

<TopHeader selectedYear={selectedYear} selectYear={selectYear} />

{#if selectedYear === "2001-2003"}
  <main>
    <RetroComponent />
  </main>
{:else if selectedYear === "2019"}
  <ForbiddenComponent />
{:else if selectedYear === "2020"}
  <NotFoundComponent />
{:else if selectedYear === "2024-2026"}
  <IframeComponent src="https://tone-track.uno/" />
{/if}

<style>
  :root {
    --background-color: black;
  }

  main {
    background: var(--background-color);
  }
</style>
