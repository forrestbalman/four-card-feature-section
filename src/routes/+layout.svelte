<script>
  import favicon from "$lib/assets/favicon-32x32.png";

  let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins:wght@200;400;600&display=swap"
    rel="stylesheet"
  />
</svelte:head>

<main>
  {@render children()}
</main>

<style>
  :global(:root) {
    font-family: "Poppins", sans-serif;

    --red: hsl(0, 78%, 62%);
    --cyan: hsl(180, 62%, 55%);
    --orange: hsl(34, 97%, 64%);
    --blue: hsl(212, 86%, 64%);
    --grey-500: hsl(234, 12%, 34%);
    --grey-400: hsl (212, 6%, 44%);
    --white: hsl(0, 0%, 100%);
  }

  main {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>
