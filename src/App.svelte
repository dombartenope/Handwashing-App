<script>
  import HowTo from "./HowTo.svelte";
  import Timer from "./Timer.svelte";

  let name = "Dom";
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Dosis&display=swap");

  :global(body) {
    font-family: "Dosis", sans-serif;
  }

  :global(button) {
    border: none;
    color: #fff;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    outline: none;
    flex: 1;
    cursor: pointer;
  }

  h1 {
    font-size: 4em;
    font-weight: 100;
    color: #f33f33;
    text-align: center;
    text-transform: uppercase;
  }
  h3 {
    font-size: 1em;
    font-weight: 100;
    text-align: center;
  }
</style>

<h1>Handwashing Timer</h1>
<Timer />
<HowTo />

<h3>
  <a href="https://www.who.int/gpsc/clean_hands_protection/en/">
    Picture Source
  </a>
  |
  <a href="https://freesound.org/people/metrostock99/sounds/345086/">
    Sound Source
  </a>
</h3>
