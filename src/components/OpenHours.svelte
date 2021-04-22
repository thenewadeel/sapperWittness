<script>
  import CTA from '../components/CTA.svelte';
  import Title from '../components/PageTitle.svelte';
</script>

<style>
  section {
    padding: 72px 0;
    background-image: url('open-hours.webp');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    text-align: center;
    position: relative;
  }

  section:before {
    content: '';
    background: rgba(25, 32, 46, 0.5);
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    z-index: 1;
  }

  .info {
    color: #fff;
    line-height: 1.7em;
    margin-bottom: 20px;
    z-index: 2;
    position: relative;
  }

  .info:last-of-type {
    margin-bottom: 40px;
  }

  @media (min-width: 992px) {
    .info {
      font-size: 1.5em;
    }
  }
</style>

<section>
  <Title title="Reserve a Meet" subTitle="Consultation Hours" theme="title-white" />

  <p class="info">Saturday – Sunday: 10 AM – 3 PM</p>

  <CTA linkHref="#" linkTheme="link-light" linkTitle="Book now" />

</section>
