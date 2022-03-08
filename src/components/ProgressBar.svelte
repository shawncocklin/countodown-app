<script>
  export let progress = 0
</script>

<div bp="grid">
  <div bp="offset-5@md 4@md 12@sm" class="progress-container">
    <div class="progress-bar" style="width: {progress}%;">
      <span class="sr-only">{progress}%</span>
    </div>
  </div>
</div>

<style>
  .progress-container {
    margin: 1.25rem 0;
    border: 1px solid #b4b4b4;
  }

  .progress-bar {
    height: 2rem;
    background-color: green;
  }
</style>
