<script lang="ts">
	import Logo from "./Logo.svelte";
	import About from "./About.svelte";
	import Smoke from './Smoke.svelte';
	import Instagram from './icons/Instagram.svelte';
	import Twitter from './icons/Twitter.svelte';
	import Soundcloud from './icons/Soundcloud.svelte';
	import Spotify from './icons/Spotify.svelte';

	let showAbout = false

	const handleAboutClick = () => {
		showAbout = true
	}

	const handleOuterClick = () => {
		if (showAbout) {
			showAbout = false
		}
	}
	
</script>

<main>
	<!-- <Header /> -->
	<div id='big-wrapper'>
		<img src='https://i.imgur.com/XN45Woe.jpg' />
		<div class='rounded-box'>
			<div class='smoke-wrapper'>
				<Smoke />
			</div>
			<Logo />
			{#if showAbout}
				<About
					onHide={() => showAbout = false}
				/>
			{/if}
			<div id='social-links'>
				<a href='https://urlgeni.us/instagram/ZECUellimist' class='add-15' target='blank'>
					<Instagram ref='instaHome' size={30} />
				</a>
				<a href='https://urlgeni.us/twitter/Qu2Uellimist' class='add-15' target='blank'>
					<Twitter ref='twitterHome' size={30} />
				</a>
				<a href='https://urlgeni.us/soundcloud/zhTRellimist' class='add-15' target='blank'>
					<Soundcloud ref='soundcloudHome' size={30} />
				</a>
				<a href='https://urlgeni.us/soundcloud/zhTRellimist' target='blank'>
					<Spotify ref='spotifyHome' size={32} />
				</a>
			</div>
		</div>
	</div>
	<div id='contact-wrapper'>
		<a id='about' class='nav' on:click={handleAboutClick}>ABOUT</a>
		<a id='contact' class='nav' href="mailto:alex@ellimistmusic.com">CONTACT</a>
		<a id='florish' class='nav' target='blank' href="https://soundcloud.com/ellimistmusic/florish">LISTEN TO FLORISH</a>
	</div>
</main>

<style>
	.add-15 {
		margin-bottom: 15px ;
	}

	#contact-wrapper {
		width: 100%;
		height: 80px;
		padding: 0 80px;
		position: absolute;
		display: flex;
		justify-content: flex-start;
		align-items: center;
		bottom: 0;
	}

	.nav {
		display: flex;
		align-items: center;
		height: 100%;
		font-size: 1em;
		letter-spacing: .5em;
		color: rgb(64, 64, 64);
		text-decoration: none;
		margin-right: 80px;
		font-family: "Trebuchet MS";
	}

	.nav:hover {
		cursor: pointer;
		color: rgba(#6ae8f9, .5);
	}

	#social-links {
		position: absolute;
		display: flex;
		flex-direction: column;
		top: 10px;
		left: 10px;
	}

	@keyframes pulse-color {
    0% { color: rgba(#6ae8f9, .3); }
    17% { color: rgba(#6ae8f9, .25); }
    25% { color: rgba(#6ae8f9, .1); }
    33% { color: rgba(#6b67ee, .25); }
    50% { color: rgba(#6b67ee, .3); }
    67% { color: rgba(#6b67ee, .25); }
    75% { color: rgba(#6b67ee, .1); }
    83% { color: rgba(#6ae8f9, .25); }
    100% { color: rgba(#6ae8f9, .3); }
  }

	img {
		position: absolute;
		bottom: 20px;
		right: 20px;
		width: 60px;
		height: auto;
	}

	.smoke-wrapper {
		position: absolute;
		top: 0;
		left: 0;
		height: 100%;
		width: 100%;
		border-radius: inherit;
	}

	main {
		text-align: center;
		margin: 0 auto;
	}

	#big-wrapper {
		display: flex;
		width: 100%;
		height: calc(100vh);
		justify-content: center;
		align-items: center;
	}

	.rounded-box {
		width: calc(100% - 160px);
		height: calc(100% - 160px);
		display: flex;
		justify-content: center;
		align-items: center;
		border: 1px solid white;
		border-radius: 9px;
		overflow: hidden;
		position: relative;
	}

	@media screen and (max-width: 660px) {
		.rounded-box {
			width: calc(100% - 70px);
			height: calc(100% - 70px);
		}
	}
</style>
