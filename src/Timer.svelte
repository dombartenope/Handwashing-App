<script>
  import ProgressBar from "./ProgressBar.svelte";

  const totalSeconds = 20;

  let secondsLeft = totalSeconds;

  $: inverseSeconds = ((totalSeconds - secondsLeft) / totalSeconds) * 100;

  let isRunning = false;

  function handleClick() {
    isRunning = true;
    const timer = setInterval(() => {
      if (secondsLeft > 0) {
        inverseSeconds += 1;
        secondsLeft -= 1;
      } else {
        clearInterval(timer);
        isRunning = false;
        secondsLeft = totalSeconds;
      }
    }, 1000);
  }
</script>

<style>
  h2 {
    margin: 0;
  }

  .start {
    background-color: #bd2217;
    width: 100%;
    margin: 10px 0;
  }

  .start[disabled] {
    background-color: rgb(194, 194, 194);
    cursor: not-allowed;
  }
</style>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondsLeft}</h2>
</div>

<ProgressBar progress={inverseSeconds} />

<div bp="grid">
  <button
    disabled={isRunning}
    bp="offset-5@md 4@md 12@sm"
    class="start"
    on:click={handleClick}>
    Start
  </button>
</div>
