<script>
  import HeroBanner from '../components/HeroBanner.svelte';
  import Overview from '../components/Overview.svelte';
  import OpenHours from '../components/OpenHours.svelte';
</script>

<style>

</style>

<svelte:head>
  <title>Wittness Tech</title>
</svelte:head>

<div>
  <HeroBanner
    bannerTitle="Wittness Tech"
    bannerSubtitle="Improving lives - bit by bit"
    themeBannerFullHeight
    bannerImg="homepage" />
  <Overview />
  <OpenHours />
</div>
