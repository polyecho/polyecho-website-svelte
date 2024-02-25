<script lang="ts">
	import '../lib/reset.css';
	import '../lib/fonts.css';
	import { base } from '$app/paths';
</script>

<svelte:head>
	<title>Echo</title>
	<meta name="theme-color" content="#11DC9F" />
	<meta name="description" content="Echo observer." />

	<meta property="og:type" content="website" />
	<meta property="og:title" content="Echo" />
	<meta property="og:description" content="Echo observer." />
	<meta property="og:image" content="{base}/images/thumbnail.png" />
	<meta property="og:url" content="https://polyecho.com/" />

	<meta name="twitter:title" content="Echo" />
	<meta name="twitter:description" content="Echo observer." />
	<meta name="twitter:image" content="{base}/images/thumbnail.png" />
	<meta name="twitter:card" content="summary_large_image" />

	<link rel="icon" href="{base}/favicon.png" type="image/png" />
	<link rel="apple-touch-icon" href="{base}/images/logo192.png" />
</svelte:head>
<slot />

<style lang="scss">
	:global(body) {
		background-color: #02140f;
		color: #17e8b7;
		height: 100vh;
		margin: 0;
		padding: 0;
	}
</style>
