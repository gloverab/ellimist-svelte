<script lang='ts'>
  export let onHide
</script>

<p><button on:click={onHide}>X</button>&nbsp;Ellimist is an organic elecronic music project</p>

<style>
  p {
    font-size: 1.5em;
    position: absolute;
    bottom: 200px;
    color: rgb(64, 64, 64);
  }

  button {
    color: red;
  }
</style>