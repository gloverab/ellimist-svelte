<script lang='ts'>

</script>

<div id='scene'>
  <div id='logo-glitch-1-wrapper' class='glitch-wrapper one'>
    <div id='logo-glitch-1' class='glitch-block one' />
  </div>
  <div id='logo-glitch-2-wrapper' class='glitch-wrapper two'>
    <div id='logo-glitch-2' class='glitch-block two' />
  </div>
  <div id='logo-glitch-3-wrapper' class='glitch-wrapper three'>
    <div id='logo-glitch-3' class='glitch-block three' />
  </div>
  <div id='word-wrapper'>
    <h1>ELLIMIST</h1>
  </div>
</div>


<style lang='scss'>
  $primary-color: #6ae8f9;
	$secondary-color: #6b67ee;

  #scene {
		width: 100%;
		height: 100%;
		position: relative;
		display: flex;
		// justify-content: center;
		align-items: center;
	}

	div {
		animation: glitch 1s linear infinite;
	}

	.glitch-wrapper {
		position: absolute;
		top: 0;
		bottom: 0;
		height: 100%;

		&.one {
			width: 100px;
			animation: move-block 7s infinite linear;
		}

		&.two {
			width: 12px;
			animation: move-block 9s infinite linear;
		}

		&.three {
			width: 12px;
			animation: move-block-2 10s infinite linear;
		}
	}

	.glitch-block {
		width: 100%;
		height: 100%;
		
		&.one {
			animation: background-colors 2s infinite;
		}

		&.two {
			animation: background-colors 3s infinite;
		}

		&.three {
			animation: background-colors 1.5s infinite;
		}
	}

  #word-wrapper {
		height: 100%;
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
    animation: adjust-opacity 8s linear infinite;
  }

  h1 {
		color: black;
		text-transform: uppercase;
		font-size: 12rem;
		font-weight: 400;
		position: relative;
		animation: text-glow-1 7s infinite linear;
		margin-top: -10rem;

    &:hover {
			cursor: default;
		}
	}

  @keyframes adjust-opacity {
    0% {
      opacity: 1;
    }
    33% {
      opacity: .4;
    }
    66% {
      opacity: .9;
    }
    90% {
      opacity: .2;
    }
    100% {
      opacity: 1;
    }
  }

  @keyframes text-glow-1 {
    0%, 2%, 8%, 10%, 100% {
      text-shadow: none;
      transform: translate3d(20px,60px,0)
    }

    1%, 9% {
      text-shadow: .01em .01em mix(#0f0f0f, $primary-color, 64%);
      transform: translate3d(20px,60px,0)
    }
  }

  @keyframes text-glow-2 {
    0%, 1%, 3%, 12%, 14%, 100% {
      text-shadow: none;
      transform: translate3d(20px,60px,0)
    }

    2%, 13% {
      text-shadow: .03em .03em mix(#fff, $primary-color, 64%);
      transform: translate3d(20px,60px,0)
    }
  }

  @keyframes move-block {
		0% { transform: translate3d(0, 0, 0) }
		50% { transform: translate3d(400px, 0, 0) }
		100% { transform: translate3d(900px, 0, 0) }
	}

  @keyframes move-block-2 {
		0% { transform: translate3d(0, 0, 0) scaleX(1) }
		41% { transform: translate3d(200px, 0, 0) scaleX(1) }
		42% { transform: translate3d(210px, 0, 0) scaleX(25) }
		49% { transform: translate3d(210px, 0, 0) scaleX(20) }
		50% { transform: translate3d(400px, 0, 0) scaleX(1) }
		84% { transform: translate3d(780px, 0, 0) scaleX(1) }
		85% { transform: translate3d(800px, 0, 0) scaleX(15) }
		100% { transform: translate3d(900px, 0, 0) scaleX(1) }
	}

	@keyframes background-colors {
		0% { background-color: black; }
		13% { background-color: black; }
		14% { background-color: rgba($primary-color, .2); }
		15% { background-color: black; }
		20% { background-color: rgba($primary-color, .2); }
		21% { background-color: black; }
		28% { background-color: black; }
		29% { background-color: rgba($primary-color, .1); }
		30% { background-color: black; }
		35% { background-color: black; }
		36% { background-color: rgba($primary-color, .4); }
		38% { background-color: black; }
		43% { background-color: black; }
		44% { background-color: rgba($primary-color, .02); }
		45% { background-color: black; }
		46% { background-color: rgba($primary-color, .01); }
		47% { background-color: black; }
		48% { background-color: black; }
		49% { background-color: rgba($primary-color, .01); }
		50% { background-color: black; }
		51% { background-color: black; }
		52% { background-color: black; }
		53% { background-color: black; }
		54% { background-color: black; }
		55% { background-color: rgba($primary-color, .02); }
		56% { background-color: rgba($primary-color, .01); }
		57% { background-color: rgba($primary-color, .06); }
		58% { background-color: black; }
		59% { background-color: rgba($primary-color, .02); }
		60% { background-color: black; }
		61% { background-color: black; }
		62% { background-color: black; }
		63% { background-color: black; }
		64% { background-color: black; }
		65% { background-color: rgba($primary-color, .1); }
		66% { background-color: black; }
		67% { background-color: black; }
		68% { background-color: rgba($primary-color, .02); }
		69% { background-color: rgba($primary-color, .06); }
		70% { background-color: black; }
		71% { background-color: black; }
		72% { background-color: rgba($primary-color, .35); }
		73% { background-color: black; }
		74% { background-color: rgba($primary-color, .08); }
		75% { background-color: rgba($primary-color, .01); }
		76% { background-color: black; }
		77% { background-color: rgba($primary-color, .03); }
		78% { background-color: black; }
		79% { background-color: black; }
		80% { background-color: rgba($primary-color, .01); }
		81% { background-color: black; }
		82% { background-color: rgba($primary-color, .02); }
		83% { background-color: rgba($primary-color, .1); }
		84% { background-color: $primary-color; }
		85% { background-color: black; }
		86% { background-color: black; }
		87% { background-color: black; }
		88% { background-color: black; }
		89% { background-color: black; }
		90% { background-color: black; }
		91% { background-color: black; }
		92% { background-color: rgba($primary-color, .07); }
		93% { background-color: black; }
		94% { background-color: rgba($primary-color, .01); }
		95% { background-color: black; }
		96% { background-color: black; }
		97% { background-color: rgba($primary-color, .13); }
		98% { background-color: black; }
		99% { background-color: black; }
		100% { background-color: black; }
	}

  // @keyframes text-glow-1 {
	// 	0% {
	// 		text-shadow: -0.01em 0 rgba($secondary-color, .3);
	// 	}
	// 	1% {
	// 		text-shadow: .01em .01em mix(#fff, $primary-color, 64%);
	// 	}
  //   2% {
  //     text-shadow: none;
  //   }
  //   9% {
  //     text-shadow: none;
  //   }
  //   10% {
	// 		text-shadow: -.02em -.02em mix(#fff, $primary-color, 40%);
	// 	}
  //   11% {
  //     text-shadow: none;
  //   }
	// 	100% {
	// 		text-shadow: none;
	// 	}
	// }

  @keyframes glitch{
		2%,64%{
			transform: translate(2px,0) skew(0deg);
		}
		4%,60%{
			transform: translate(-2px,0) skew(0deg);
		}
		62%{
			transform: translate(0,0) skew(5deg); 
		}
	}

	div:before,
	div:after{
		content: attr(title);
		position: absolute;
		left: 0;
	}

	div:before{
		animation: glitchTop 1s linear infinite;
		clip-path: polygon(0 0, 100% 0, 100% 33%, 0 33%);
		-webkit-clip-path: polygon(0 0, 100% 0, 100% 33%, 0 33%);
	}

	@keyframes glitchTop{
		2%,64%{
			transform: translate(2px,-2px);
		}
		4%,60%{
			transform: translate(-2px,2px);
		}
		62%{
			transform: translate(13px,-1px) skew(-13deg); 
		}
	}

	div:after{
		animation: glitchBotom 1.5s linear infinite;
		clip-path: polygon(0 67%, 100% 67%, 100% 100%, 0 100%);
		-webkit-clip-path: polygon(0 67%, 100% 67%, 100% 100%, 0 100%);
	}

	@keyframes glitchBotom{
		2%,64%{
			transform: translate(-2px,0);
		}
		4%,60%{
			transform: translate(-2px,0);
		}
		62%{
			transform: translate(-22px,5px) skew(21deg); 
		}
	}

	@media only screen and (max-width: 600px) {
		h1 {
			font-size: 6em;
		}
	}

</style>