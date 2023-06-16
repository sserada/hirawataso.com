<script lang="ts">
  import Header from "../components/Header.svelte";
  const logoPath: string = "/logo.svg"
</script>

<main>
  <Header />
  <img src={logoPath} class="logo" alt="logo">
  <div class="underline"></div>
</main>

<style lang="scss">
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 90vh;
    .logo {
      width: 30%;
      pointer-events: none;
      filter: drop-shadow(0 0 0.75rem #333);
      margin-bottom: 2rem;
    }
    .underline {
      width: 10%;
      height: 1px;
      background-color: #333;
      filter: drop-shadow(0 0 0.75rem #333);
    }
  }
</style>

