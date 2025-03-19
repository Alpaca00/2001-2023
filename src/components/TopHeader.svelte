<script>
  export let selectedYear;
  export let selectYear;

  export let years = [
    { label: "2001-2003", disabled: false },
    { label: "2004-2007", disabled: true },
    { label: "2008-2011", disabled: true },
    { label: "2012-2015", disabled: true },
    { label: "2016-2019", disabled: true },
    { label: "2021-2023", disabled: true },
    { label: "2024-2026", disabled: false },
  ];

  function handleYearSelect(yearLabel) {
    selectYear(yearLabel);
  }
</script>

<div class="top-header">
  <div class="year-links">
    {#each years as year}
      <a
        href="#"
        class="year-link {selectedYear === year.label ? 'active' : ''}"
        on:click|preventDefault={() => handleYearSelect(year.label)}
        class:disabled={year.disabled}
      >
        {year.label}
      </a>
    {/each}
  </div>
</div>

<style>
  .top-header {
    display: flex;
    justify-content: center;
    gap: 15px;
    padding: 10px;
    background-color: black;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    font-size: 18px;
  }

  .year-links {
    display: flex;
    gap: 15px;
  }

  .year-link {
    color: #00ff00;
    font-weight: bold;
    text-decoration: none;
    cursor: pointer;
  }

  .year-link.active {
    color: #ffcc00;
  }

  .year-link:hover {
    text-decoration: underline;
  }

  .year-link.disabled {
    color: #ccc;
    cursor: not-allowed;
  }
</style>
