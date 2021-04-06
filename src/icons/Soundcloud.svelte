<script lang='ts'>
  export let fill
  export let size
  export let ref
  export let hoverFill
</script>

<svg xmlns="http://www.w3.org/2000/svg" width={size} height={size} viewBox="0 0 24 24">
  <path d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm-6.417 14.583c-.354-.318-.583-.79-.583-1.323 0-.532.229-1.003.583-1.323v2.646zm1.167.417c-.212 0-.323.003-.583-.08v-3.318c.276-.088.407-.085.583-.071v3.469zm1.167 0h-.584v-3.305l.18.105c.08-.328.222-.628.404-.895v4.095zm1.166 0h-.583v-4.706c.18-.134.373-.25.583-.33v5.036zm1.167 0h-.583v-5.167c.22-.023.286-.04.583.005v5.162zm1.167 0h-.584v-4.987l.222.107c.104-.181.228-.346.362-.5v5.38zm5.885 0h-5.302v-5.904c.465-.32 1.016-.512 1.611-.512 1.583 0 2.866 1.307 2.984 2.962 1.14-.558 2.405.34 2.405 1.642 0 1-.761 1.812-1.698 1.812z"/>
</svg>

<style lang='scss'>
  svg path {
    fill: rgb(64, 64, 64);
    animation: none;
    transition: .3s ease all;
  }

  svg:hover path {
    fill: rgba(#6ae8f9, .3);

    animation: pulse-fill 3s linear infinite;
  }

  @keyframes pulse-fill {
	0% { fill: rgba(#6ae8f9, .3); }
	17% { fill: rgba(#6ae8f9, .25); }
	25% { fill: rgba(#6ae8f9, .1); }
	33% { fill: rgba(#6b67ee, .25); }
	50% { fill: rgba(#6b67ee, .3); }
	67% { fill: rgba(#6b67ee, .25); }
	75% { fill: rgba(#6b67ee, .1); }
	83% { fill: rgba(#6ae8f9, .25); }
	100% { fill: rgba(#6ae8f9, .3); }
}
</style>