<script lang="ts">
	import { onMount } from 'svelte'
  import SmokeMachine from '@bijection/smoke'
  
  let party
  let canvas
  let mouseOverCanvas

  const onMouseMove = (e) => {
    if (mouseOverCanvas) {
      var x = e.clientX
      var y = e.clientY
      var n = 5
      var t = Math.floor(Math.random() * 200) + 3800

      party.addsmoke(x, y, n, t)
    }

  }
  
  onMount(() => {
    var ctx = canvas.getContext('2d')
    canvas.width = 1000
    canvas.height = 500
    console.log(SmokeMachine)
    party = SmokeMachine(ctx, [20, 20, 20])
    
    party.start() // start animating
    
    party.addSmoke(500,500,10) // wow we made smoke
    
    setTimeout(function(){
    
      // party.stop() // stop animating
    
      party.addSmoke(500,500,100)
      party.addSmoke(500,500,20)
    
      for(var i=0;i<10;i++){
        party.step(10) // pretend 10 ms pass and rerender
      }
    
      setTimeout(function(){
        party.start()
      },1000)
    
    },1000)
  })

</script>

<svelte:window on:mousemove={onMouseMove} />

<canvas bind:this={canvas} on:mouseleave={() => mouseOverCanvas = false} on:mouseenter={() => mouseOverCanvas = true} />

<style>
  canvas {
    width: 100%;
    height: 100%;
    position: absolute;
    bottom: 0;
    left: 0;
    border-radius: inherit;
  }
</style>