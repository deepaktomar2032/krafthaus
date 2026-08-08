<script>
  import { company } from '$lib/data/company'
</script>

<svelte:head>
  <title>Privacy Policy | {company.displayName}</title>
  <meta name="description" content={`Privacy Policy for ${company.legalName}`} />
</svelte:head>

<article class="container legal">
  <span class="section-eyebrow">Legal</span>
  <h1>Privacy Policy</h1>
  <p class="updated">Last updated: August 2026</p>

  <p>
    {company.legalName} ("Krafthaus," "we," "us," or "our") respects your privacy. This Privacy Policy explains what
    information we collect, how we use it, and the choices you have — including with respect to SMS/text messaging
    communications.
  </p>

  <h2>Information We Collect</h2>
  <p>We collect information you provide directly to us, such as:</p>
  <ul>
    <li>Your name and email address when you contact us.</li>
    <li>Your mobile phone number if you opt in to receive text messages from us.</li>
  </ul>

  <h2>How We Use Your Information</h2>
  <p>We use the information we collect to:</p>
  <ul>
    <li>Respond to your inquiries and requests.</li>
    <li>Send order, shipping, and delivery updates by SMS to customers who have opted in.</li>
    <li>Operate, maintain, and improve our business and websites.</li>
  </ul>

  <h2>SMS/Text Messaging Program</h2>
  <p>
    Message frequency varies depending on your order and account activity. Message and data rates may apply. You can
    opt out of text messages at any time by replying <strong>STOP</strong>. For help, reply <strong>HELP</strong> or
    contact us at <a href={`mailto:${company.email}`}>{company.email}</a>. Carriers are not liable for delayed or
    undelivered messages.
  </p>

  <h2>No Sharing of Mobile Information</h2>
  <p>
    No mobile information will be shared with third parties or affiliates for marketing or promotional purposes. All
    other categories of information described in this policy exclude text messaging originator opt-in data and
    consent — this information will not be shared with any third parties for any purpose.
  </p>

  <h2>Data Security</h2>
  <p>
    We take reasonable measures to protect the information we collect from loss, misuse, and unauthorized access. No
    method of transmission or storage is completely secure, and we cannot guarantee absolute security.
  </p>

  <h2>Your Choices</h2>
  <p>
    You may opt out of SMS communications at any time by replying STOP to any message, and you may contact us at
    <a href={`mailto:${company.email}`}>{company.email}</a> with any questions about your information or to request
    its deletion.
  </p>

  <h2>Changes to This Policy</h2>
  <p>
    We may update this Privacy Policy from time to time. Changes will be posted on this page with an updated
    effective date.
  </p>

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
