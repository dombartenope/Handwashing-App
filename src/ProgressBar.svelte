<script>
  export let progress = 20;
</script>

<style>
  .sr-only {
    display: none;
  }

  .progress-container {
    margin: 20px 0;
    border: 1px solid rgb(194, 194, 194);
  }

  .progress-bar {
    background-color: rgb(77, 199, 55);
    height: 30px;
  }
</style>

<div bp="grid">
  <div bp="offset-5@md 4@md 12@sm" class="progress-container">
    <div style="width: {progress}%;" class="progress-bar">
      <span class="sr-only" style="width: {progress}%;">%</span>
    </div>
  </div>
</div>
