<script>
  import { createEventDispatcher } from 'svelte'
  import ProgressBar from './ProgressBar.svelte'
  const totalSeconds = 20
  const dispatch = createEventDispatcher()
  let secondsLeft = totalSeconds
  let isRunning = false
  $: progress = ((totalSeconds - secondsLeft) / totalSeconds) * 100

  function countdown() {
    isRunning = true
    const timer = setInterval(() => {
      secondsLeft--

      if (secondsLeft === 0) {
        clearInterval(timer)
        isRunning = false
        secondsLeft = totalSeconds
        dispatch('end')
      }
    }, 1000)
  }
</script>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondsLeft}</h2>
</div>

<ProgressBar {progress} />

<div bp="grid">
  <button
    disabled={isRunning}
    class="start"
    bp="offset-5@md 4@md 12@sm"
    on:click={countdown}>Start</button
  >
</div>

<style>
  h2 {
    margin: 0;
  }
  .start {
    background-color: rgb(154, 73, 73);
    width: 100%;
    margin: 0.875rem 0;
  }
  .start:disabled {
    background-color: rgba(154, 73, 73, 0.5);
  }
</style>
