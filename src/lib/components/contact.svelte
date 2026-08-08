<script>
  import { company } from '$lib/data/company'
</script>

<section id="contact" class="alt-background">
  <div class="container contact-inner">
    <span class="section-eyebrow">Contact</span>
    <h2 class="section-title">Let's talk</h2>
    <p class="section-description">
      For partnership, sourcing, or general inquiries, reach us directly by email.
    </p>
    <a class="button-primary" href={`mailto:${company.email}`}>{company.email} →</a>
  </div>
</section>

<style lang="scss">
  section {
    padding: 72px 0;
  }

  .alt-background {
    background: var(--section-alt-background);
  }

  .contact-inner {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;

    .section-description {
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>
