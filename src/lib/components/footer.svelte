<script>
  import { company } from '$lib/data/company'

  let currentYear = new Date().getFullYear()
</script>

<footer>
  <div class="container">
    <div class="grid">
      <div class="brand-col">
        <div class="wordmark">{company.displayName}</div>
        <p class="tagline">{company.tagline}</p>
      </div>

      <div class="col">
        <div class="col-title">Contact</div>
        <a class="row" href={`mailto:${company.email}`}>{company.email}</a>
        <div class="row">{company.phone}</div>
      </div>

      <div class="col">
        <div class="col-title">Registered Address</div>
        <div class="row">{company.address.street}</div>
        <div class="row">{company.address.cityStateZip}</div>
        <div class="row">{company.address.country}</div>
      </div>
    </div>

    <div class="divider" />

    <div class="bottom-row">
      <div>© {currentYear} {company.legalName}. All rights reserved.</div>
    </div>
  </div>
</footer>

<style lang="scss">
  @use '../scss/breakpoints' as *;

  footer {
    background: var(--footer-background);
    color: var(--footer-text-color);
    padding: 56px 0 28px;
  }

  .grid {
    display: grid;
    grid-template-columns: 1.4fr 1fr 1fr;
    gap: 32px;

    @include for-tablet-down {
      grid-template-columns: 1fr;
      gap: 28px;
    }
  }

  .brand-col {
    .wordmark {
      font-family: Georgia, 'Iowan Old Style', 'Palatino Linotype', Palatino, serif;
      font-size: 1.15rem;
      font-weight: 500;
      letter-spacing: 0.18em;
      color: var(--footer-heading-color);
      margin-bottom: 10px;
    }

    .tagline {
      font-size: 0.9rem;
      max-width: 320px;
    }
  }

  .col-title {
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--footer-heading-color);
    margin-bottom: 12px;
  }

  .row {
    display: block;
    font-size: 0.9rem;
    color: var(--footer-text-color);
    text-decoration: none;
    margin-bottom: 6px;

    &:hover {
      color: #ffffff;
    }
  }

  .divider {
    height: 1px;
    background: rgba(255, 255, 255, 0.12);
    margin: 40px 0 20px;
  }

  .bottom-row {
    font-size: 0.82rem;
    color: rgba(255, 255, 255, 0.55);
  }
</style>
