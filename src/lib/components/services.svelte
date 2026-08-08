<script>
  import { services } from '$lib/data/services'
</script>

<section id="services" class="alt-background">
  <div class="container">
    <span class="section-eyebrow">What We Do</span>
    <h2 class="section-title">End-to-end e-commerce operations</h2>
    <p class="section-description">
      From sourcing to the customer's doorstep, we run the pieces that make an online retail brand work.
    </p>
    <div class="grid">
      {#each services as service}
        <div class="card">
          <h3>{service.title}</h3>
          <p>{service.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style lang="scss">
  @use '../scss/breakpoints' as *;

  section {
    padding: 72px 0;
  }

  .alt-background {
    background: var(--section-alt-background);
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;

    @include for-phone-only {
      grid-template-columns: 1fr;
    }
  }

  .card {
    background: var(--card-background);
    border-radius: 10px;
    padding: 28px;
    box-shadow: var(--card-shadow);

    h3 {
      font-size: 1.05rem;
      font-weight: 700;
      color: var(--navy);
      margin-bottom: 10px;
    }

    p {
      font-size: 0.9rem;
      color: var(--text-light-color);
    }
  }
</style>
