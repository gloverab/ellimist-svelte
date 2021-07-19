<script lang='ts'>
  export let onHide
</script>

<div id='about'>
  <p><button on:click={onHide}>X</button>&nbsp;Ellimist is the Boston-bsaed multifaceted artist focused on creating organic electronic music that moves the body and mind. Known for his behind-the-scenes production work with violinist Josh Knowles and his instrumental prowess with It Was a Good Dream and Weird Phishes, the Ellimist project is where it all comes together for Alex Glover.</p>
  <p>Equal parts sound design, composition, and musicianship, Ellimist's music transports listeners on a journey through a combination of ambient melodies and bone rattling bass that flirts with funk, house, dubstep, and everything in between.</p>
</div>

<style>
  #about {
    position: absolute;
    bottom: 200px;
  }

  p {
    font-size: 1.5em;
    color: rgb(64, 64, 64);
    text-align: left;
  }

  p:not(:last-of-type) {
    margin-bottom: 1rem;
  }

  button {
    color: red;
  }
</style>