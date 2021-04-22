<script>
  import OpenHours from '../components/OpenHours.svelte';
  import CTA from '../components/CTA.svelte';
  import Title from '../components/PageTitle.svelte';
  import HeroBanner from '../components/HeroBanner.svelte';

  let showMore = false;

  function handleShowMore() {
    showMore ? (showMore = false) : (showMore = true);
  }
</script>

<style>
  section {
    padding-top: 54px;
    padding-bottom: 32px;
    text-align: center;
    background-color: #f4f4f4;
  }

  .subtitle {
    font-size: 24px;
    font-style: italic;
    line-height: 40px;
    font-weight: 400;
    margin-bottom: 40px;
  }

  p {
    margin-bottom: 16px;
  }

  .grid-item:first-child {
    margin-bottom: 40px;
  }

  .grid-item:last-child {
    margin-bottom: 50px;
  }

  img {
    max-width: 100%;
  }

  .hidden {
    display: none;
  }

  @media only screen and (min-width: 992px) {
    .grid {
      display: grid;
      column-gap: 50px;
      grid-template-columns: 1fr 1fr;
    }

    section {
      text-align: left;
    }
  }
</style>

<svelte:head>
  <title>Contact Us</title>
</svelte:head>

<HeroBanner
  bannerSubtitle="A modern tech company focussed on premium solutions"
  bannerTitle="Contact Us"
  bannerImg="contact" />
<section>
  <div class="container">

    <div class="grid">
      <div class="grid-item">
        <Title title="Get in touch for feedback" subTitle="Contact Us" theme="title-dark" />

        <!-- <CTA
          linkTheme="link-dark"
          linkTitle={showMore ? 'Hide' : 'More. . .'}
          on:click={handleShowMore} /> -->

      </div>
      <div class="grid-item">
        <img src="/client/contact-us.webp" alt="" />
        <p>

          Do write
        </p>
      </div>
    </div>
  </div>

</section>
