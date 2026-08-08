<script>
  import { company } from '$lib/data/company'
</script>

<svelte:head>
  <title>Terms & Conditions | {company.displayName}</title>
  <meta name="description" content={`Terms and Conditions for ${company.legalName}`} />
</svelte:head>

<article class="container legal">
  <span class="section-eyebrow">Legal</span>
  <h1>Terms & Conditions</h1>
  <p class="updated">Last updated: August 2026</p>

  <p>
    These Terms & Conditions ("Terms") govern your use of the {company.displayName} website and any SMS/text
    messaging program offered by {company.legalName} ("Krafthaus," "we," "us," or "our"). By using our website or
    opting in to our text messaging program, you agree to these Terms.
  </p>

  <h2>About Krafthaus</h2>
  <p>
    {company.legalName} is a US-based e-commerce company that operates digital-first retail brands across online
    marketplaces and direct-to-consumer storefronts.
  </p>

  <h2>SMS/Text Messaging Program</h2>
  <p>Our text messaging program sends order confirmations, shipping and delivery status updates, and related account notifications.</p>
  <ul>
    <li><strong>Opt-in:</strong> You opt in to this program by providing your mobile number and consent through our website or at checkout on a Krafthaus-operated storefront.</li>
    <li><strong>Message frequency:</strong> Varies based on your order and account activity.</li>
    <li><strong>Cost:</strong> Message and data rates may apply.</li>
    <li><strong>Opt-out:</strong> Text <strong>STOP</strong> at any time to stop receiving messages.</li>
    <li><strong>Help:</strong> Text <strong>HELP</strong> or email <a href={`mailto:${company.email}`}>{company.email}</a>.</li>
    <li>Carriers are not liable for delayed or undelivered messages.</li>
  </ul>
  <p>Our Privacy Policy, available at <a href="/privacy">krafthausgroup.com/privacy</a>, describes how we handle your information.</p>

  <h2>Use of Website</h2>
  <p>
    You agree to use this website only for lawful purposes and in a manner that does not infringe the rights of, or
    restrict or inhibit the use of, this website by any third party.
  </p>

  <h2>Intellectual Property</h2>
  <p>
    All content on this website, including text, graphics, and logos, is the property of {company.legalName} unless
    otherwise noted, and may not be reproduced without our prior written consent.
  </p>

  <h2>Limitation of Liability</h2>
  <p>
    To the fullest extent permitted by law, {company.legalName} shall not be liable for any indirect, incidental, or
    consequential damages arising from your use of this website or our text messaging program.
  </p>

  <h2>Governing Law</h2>
  <p>These Terms are governed by the laws of the State of Wyoming, without regard to its conflict of law principles.</p>

  <h2>Changes to These Terms</h2>
  <p>We may update these Terms from time to time. Continued use of our website or messaging program after changes are posted constitutes acceptance of the updated Terms.</p>

  <h2>Contact Us</h2>
  <p>
    {company.legalName}<br />
    {company.address.street}<br />
    {company.address.cityStateZip}<br />
    {company.address.country}<br />
    <a href={`mailto:${company.email}`}>{company.email}</a>
  </p>
</article>

<style lang="scss">
  .legal {
    max-width: 720px;
    padding-top: 64px;
    padding-bottom: 80px;

    h1 {
      font-size: clamp(1.8rem, 3.5vw, 2.3rem);
      font-weight: 800;
      color: var(--navy);
      margin-bottom: 6px;
    }

    .updated {
      font-size: 0.85rem;
      color: var(--text-light-color);
      margin-bottom: 32px;
    }

    h2 {
      font-size: 1.15rem;
      font-weight: 700;
      color: var(--navy);
      margin: 32px 0 12px;
    }

    p {
      font-size: 0.95rem;
      color: var(--text-color);
      margin-bottom: 12px;
    }

    ul {
      margin: 0 0 12px;
      padding-left: 20px;
      list-style: disc;

      li {
        font-size: 0.95rem;
        color: var(--text-color);
        margin-bottom: 6px;
      }
    }

    a {
      color: var(--gold);
      font-weight: 600;
      text-decoration: none;

      &:hover {
        text-decoration: underline;
      }
    }
  }
</style>
