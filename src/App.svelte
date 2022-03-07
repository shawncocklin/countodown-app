<script>
  import HowTo from './components/HowTo.svelte'
  import Timer from './components/Timer.svelte'
</script>

<h1>Handwashing Countdown</h1>

<Timer />
<HowTo />

<p>
  <a
    href="https://www.who.int/teams/integrated-health-services/infection-prevention-control"
    >Image Source: World Health Organization</a
  >
</p>
<p>
  <a href="https://freesound.org/people/metrostock99/sounds/345086/"
    >Sound Source: Freesound.org</a
  >
</p>

<style>
  h1,
  p {
    text-align: center;
  }

  p {
    margin: 0;
    margin-bottom: 0.25rem;
    font-weight: 800;
  }
</style>
