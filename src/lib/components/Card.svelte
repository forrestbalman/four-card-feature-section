<script>
  import { base } from "$app/paths";

  let { color, title, description, icon, alt } = $props();
</script>

<div class="card">
  <div class="edge" style={`background-color: var(--${color})`}></div>
  <div>
    <h3>{title}</h3>
    <p>{description}</p>
  </div>
  <img src="{base}/images/icon-{icon}.svg" {alt} />
</div>

<style>
  .card {
    border-radius: 10px;
    padding: 2rem;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    box-sizing: border-box;
  }

  .edge {
    width: 100%;
    height: 6px;
    position: absolute;
    top: 0;
    left: 0;
  }

  h3 {
    margin: 0;
    font-size: 24px;
    font-weight: 600;
    color: var(--grey-500);
  }

  p {
    margin: 0;
    font-weight: 400;
    font-size: 15px;
    color: var(--grey-400);
  }

  img {
    margin-top: 2rem;
    align-self: flex-end;
  }
</style>
