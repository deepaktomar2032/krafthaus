<script>
  import { company } from '$lib/data/company'
</script>

<section id="top" class="hero">
  <div class="container hero-inner">
    <span class="section-eyebrow">{company.address.country} · Est. {company.foundedYear}</span>
    <h1>{company.tagline}</h1>
    <p class="lead">{company.description}</p>
    <div class="actions">
      <a class="button-primary" href="#contact">Get in touch</a>
      <a class="button-secondary" href="#services">What we do</a>
    </div>
  </div>
</section>

<style lang="scss">
  .hero {
    padding: 96px 0 72px;
    background: linear-gradient(180deg, var(--navy-lightest) 0%, var(--page-background) 100%);
  }

  .hero-inner {
    max-width: 760px;
  }

  h1 {
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    color: var(--navy);
    margin-bottom: 20px;
  }

  .lead {
    font-size: 1.05rem;
    color: var(--text-light-color);
    margin-bottom: 32px;
  }

  .actions {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
  }

  .button-secondary {
    display: inline-flex;
    align-items: center;
    font-size: 0.95rem;
    font-weight: 600;
    color: var(--navy);
    padding: 12px 24px;
    border-radius: 6px;
    border: 1px solid var(--border-color);
    text-decoration: none;
    transition: border-color 0.2s ease;

    &:hover {
      border-color: var(--navy);
    }
  }
</style>
