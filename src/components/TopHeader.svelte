<script>
  export let years = [
    { label: "2001-2003", disabled: false },
    { label: "2004-2007", disabled: true },
    { label: "2008-2011", disabled: true },
    { label: "2012-2015", disabled: true },
    { label: "2016-2019", disabled: true },
    { label: "2020-2023", disabled: true }
  ];
</script>

<div class="top-header">
  <div class="year-links">
    {#each years as year}
      <a href="#" class="year-link {year.disabled ? 'disabled' : ''}" on:click|preventDefault={() => year.disabled ? null : alert(`Ви вибрали ${year.label}`)}>
        {year.label}
      </a>
    {/each}
  </div>
  <div class="social-links">
    <a href="https://github.com/Alpaca00" target="_blank" class="social-icon">
      <i class="fab fa-github"></i>
    </a>
    <a href="https://www.linkedin.com/in/oleg-matskiv-30b872205/" target="_blank" class="social-icon">
      <i class="fab fa-linkedin"></i>
    </a>
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

  .year-link.disabled {
    color: #666;
    cursor: not-allowed;
  }

  .year-link:hover {
    text-decoration: underline;
  }

  .social-links {
    display: flex;
    gap: 15px;
  }

  .social-icon {
    color: #00ff00;
    font-size: 24px;
    text-decoration: none;
  }

  .social-icon:hover {
    color: #ffcc00;
  }
</style>

<head>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</head>

