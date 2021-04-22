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
  <title>About - Wittness Tech</title>
</svelte:head>

<HeroBanner
  bannerSubtitle="A modern tech company focussed on premium solutions"
  bannerTitle="About Us"
  bannerImg="about" />
<section>
  <div class="container">

    <div class="grid">
      <div class="grid-item">
        <Title title="History" subTitle="About Us" theme="title-dark" />

        <p class="subtitle">
          Welcome to Wittness Tech, a modern tech company with a focus on
          premium solutions
        </p>

        <p>
          We believe that one of the strongest forces in the universe is the
          “need to create”: every time you build something out of nothing, every
          time you give shape and organization to something that has no
          structure – you are creating a miracle.
        </p>

        <p class="more" class:hidden={!showMore}>
          Wittness is an IT Services, Business Solutions Company. We strategize,
          shape and deploy leading edge solutions to assist
          organizations overcome their IT challenges. We also help them
          undertake enterprise oriented processes successfully. Focused towards
          providing high performance, low cost and accurate solutions, we believe in pushing the boundaries of software
          intelligence. Helping our clients infuse brilliance of software
          technology into their system. Our team specializes in Software Development,
          Data Analysis, Enterprise Resource Management and Education Software.
          We provide organizations design and deployment services for their
          mobile, cloud and desktop applications.
        </p>

        <CTA
          linkTheme="link-dark"
          linkTitle={showMore ? 'Hide' : 'More. . .'}
          on:click={handleShowMore} />

      </div>
      <div class="grid-item">
        <img src="/client/about-us.webp" alt="" />
      </div>
    </div>
  </div>

</section>

<OpenHours />
