<script>
  import Logo from './logo.svelte'
</script>

<header>
  <nav class="container">
    <a class="logo-link" href="/#top" aria-label="Krafthaus home">
      <Logo />
    </a>
    <div class="links">
      <a href="/#about">About</a>
      <a href="/#services">Services</a>
      <a href="/#contact" class="cta">Contact</a>
    </div>
  </nav>
</header>

<style lang="scss">
  @use '../scss/breakpoints' as *;

  header {
    position: sticky;
    top: 0;
    z-index: 100;
    padding: 16px 0;
    background: var(--header-background);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border-color);
  }

  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .logo-link {
    text-decoration: none;
  }

  .links {
    display: flex;
    align-items: center;
    gap: 28px;

    @include for-phone-only {
      gap: 16px;
    }

    a {
      font-size: 0.9rem;
      font-weight: 600;
      color: var(--text-light-color);
      text-decoration: none;
      transition: color 0.2s ease;

      &:hover {
        color: var(--navy);
      }
    }

    .cta {
      color: var(--navy);
      border: 1px solid var(--border-color);
      padding: 8px 16px;
      border-radius: 6px;

      &:hover {
        border-color: var(--navy);
      }
    }
  }
</style>
