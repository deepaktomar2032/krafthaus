<script>
  import '../lib/scss/base.scss'
  import Header from '$lib/components/header.svelte'
  import Footer from '$lib/components/footer.svelte'
  import { siteDescription, siteTitle } from '$lib/data/company'
</script>

<svelte:head>
  <title>{siteTitle}</title>
  <meta name="description" content={siteDescription} />
</svelte:head>

<Header />

<main>
  <slot />
</main>

<Footer />
