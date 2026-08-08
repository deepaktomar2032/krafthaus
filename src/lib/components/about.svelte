<script>
  import { company } from '$lib/data/company'

  const stats = [
    { value: `${company.foundedYear}`, label: 'Founded' },
    { value: 'US', label: 'Registered & operated' },
    { value: 'Multi-channel', label: 'Retail & marketplace' }
  ]
</script>

<section id="about">
  <div class="container">
    <span class="section-eyebrow">About Us</span>
    <h2 class="section-title">A US e-commerce company, built for the long run</h2>
    <p class="section-description">
      {company.legalName} operates digital-first retail brands across US online marketplaces and direct-to-consumer
      storefronts — covering sourcing, brand development, storefront operations, and fulfillment under one roof.
    </p>
    <div class="stats">
      {#each stats as stat}
        <div class="stat">
          <div class="value">{stat.value}</div>
          <div class="label">{stat.label}</div>
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

  .stats {
    display: flex;
    gap: 48px;
    flex-wrap: wrap;
    padding-top: 8px;

    @include for-phone-only {
      gap: 28px;
    }
  }

  .stat {
    .value {
      font-size: 1.4rem;
      font-weight: 800;
      color: var(--navy);
    }

    .label {
      font-size: 0.85rem;
      color: var(--text-light-color);
      margin-top: 2px;
    }
  }
</style>
