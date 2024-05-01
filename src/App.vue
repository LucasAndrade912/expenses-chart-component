<script setup></script>

<template>
  <header>
    <div class="balance-container">
      <p>My balance</p>
      <p id="balance">$921.48</p>
    </div>

    <img src="./assets/logo.svg" alt="Logo">
  </header>

  <main>
    <h1>Spending - Last 7 days</h1>
  
    mon tue wed thu fri sat sun
    
    <div class="underline" />

    <footer>
      <div>
        <span>Total this month</span>
        <strong id="amount">$478.33</strong>
      </div>

      <div id="percentage-from-last-mount">
        <strong>+2.4%</strong>
        <span>from last month</span>
      </div>
    </footer>
  </main>

  <div class="attribution">
    Challenge by
    <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
    Coded by
    <a href="https://www.github.com/LucasAndrade912" target="_blank">Lucas Andrade dos Santos</a>.
  </div>
</template>

<style scoped>
  .underline {
    width: 100%;
    height: 2px;
    background-color: var(--cream);
    margin: 2rem 0;
  }

  header {
    background-color: var(--soft-red);
    padding: 2rem;
    color: var(--very-pale-oragen);
    display: flex;
    justify-content: space-between;
    border-radius: 1.125rem;
  }

  header .balance-container #balance {
    margin-top: 8px;
    font-size: 32px;
    font-weight: 700;
  }

  main {
    background-color: var(--very-pale-oragen);
    padding: 2rem;
    border-radius: 1.125rem;
    margin: 1.5rem 0;
  }

  main h1 {
    color: var(--dark-brown);
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 1.5rem;
  }

  main footer {
    display: flex;
    justify-content: space-between;
    align-items: end;
  }

  main footer div {
    display: flex;
    flex-direction: column;
  }

  main footer div#percentage-from-last-mount {
    text-align: right;
  }

  main footer span {
    color: var(--medium-brown);
  }

  main footer strong {
    color: var(--dark-brown);
    font-weight: 700;
  }

  main footer strong#amount {
    font-size: 3rem;
  }
</style>