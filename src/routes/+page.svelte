<script>
  import Card from "$lib/components/Card.svelte";
</script>

<header>
  <h1>Reliable, efficient delivery</h1>
  <h2>Powered by Technology</h2>
  <p>
    Our artificial intelligence powered tools use millions of project data
    points to ensure that your project is successful
  </p>
</header>
<section>
  <div>
    <Card
      color="cyan"
      title="Supervisor"
      description="Monitors activity to identify project roadblocks"
      icon="supervisor"
      alt="A magnifying glass"
    />
  </div>
  <div>
    <Card
      color="red"
      title="Team Builder"
      description="Scans our talent network to create the optimal team for your project"
      icon="team-builder"
      alt="A building"
    />
  </div>
  <div>
    <Card
      color="orange"
      title="Karma"
      description="Regularly evaluates our talent to ensure quality"
      icon="karma"
      alt="A lightbulb"
    />
  </div>
  <div>
    <Card
      color="blue"
      title="Calculator"
      description="Uses data from past projects to provide better delivery estimates"
      icon="calculator"
      alt="A calculator"
    />
  </div>
</section>

<style>
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    margin: 3rem 0 3rem 0;
    max-width: 500px;
    padding: 0 3rem 0 3rem;
  }

  header h1 {
    margin: 0;
    font-weight: 200;
    font-size: 32px;
    color: var(--grey-400);
  }

  header h2 {
    margin: 0;
    margin-bottom: 1rem;
    font-weight: 600;
    font-size: 32px;
    color: var(--grey-500);
  }

  header p {
    margin: 0;
    font-weight: 400;
    font-size: 15px;
    color: var(--grey-400);
  }

  section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(4, auto);
    gap: 1.5rem;
    padding: 0 3rem 0 3rem;
  }

  section > :nth-child(1) {
    grid-area: 2 / 1 / 4 / 2;
  }
  section > :nth-child(2) {
    grid-area: 1 / 2 / 3 / 3;
  }
  section > :nth-child(3) {
    grid-area: 3 / 2 / 5 / 3;
  }
  section > :nth-child(4) {
    grid-area: 2 / 3 / 4 / 4;
  }

  @media (500px < width < 960px) {
    section {
      grid-template-columns: 1fr 1fr;
      grid-template-rows: repeat(2, minmax(300px, auto));
      padding: 0 1.5rem 0 1.5rem;
    }

    section > div:nth-child(1) {
      grid-area: 1 / 1 / 2 / 2;
    }

    section > div:nth-child(2) {
      grid-area: 1 / 2 / 2 / 3;
    }

    section > div:nth-child(3) {
      grid-area: 2 / 1 / 3 / 2;
    }

    section > div:nth-child(4) {
      grid-area: 2 / 2 / 3 / 3;
    }
  }

  @media (max-width: 500px) {
    section {
      grid-template-columns: 1fr;
      grid-template-rows: repeat(4, auto);
      padding: 0 1.5rem 0 1.5rem;
    }

    section > div {
      grid-area: auto !important;
    }
  }
</style>
