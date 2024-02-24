<script lang="ts">
	import Button from '$lib/components/Button.svelte';

	import MainLogo from '$lib/img/main-logo.svg';
	import Github from '$lib/img/github.svg';
	import Email from '$lib/img/email.svg';
	import BlueSky from '$lib/img/bluesky.svg';
	import X from '$lib/img/x.svg';

	interface Button {
		logo: string;
		url: string;
	}

	const buttons: Button[] = [
		{
			logo: `${Github}`,
			url: 'https://github.com/polyecho'
		},
		{
			logo: `${Email}`,
			url: 'mailto:echo@polyecho.com'
		},
		{
			logo: `${BlueSky}`,
			url: 'https://bsky.app/profile/polyecho.com'
		},
		{
			logo: `${X}`,
			url: 'https://twitter.com/poly_echo'
		}
	];
</script>

<div class="wrapper">
	<div class="inner-wrapper">
		<img alt="logo" class="logo" src={MainLogo} />
		<h1 class="section">Hey! It's Echo.</h1>
		<p class="section-end">There's nothing much but feel free to take a look!</p>
		{#each buttons as button}
			<Button logo={button.logo} url={button.url} />
		{/each}
	</div>
</div>

<style lang="scss">
	@keyframes floater {
		0% {
			transition: ease 0.5s;
			transform: translateY(-2px);
		}
		50% {
			transition: ease 0.5s;
			transform: translateY(10px);
		}
		100% {
			transition: ease 0.5s;
			transform: translateY(-2px);
		}
	}

	:global(body) {
		background-color: #02140f;
		color: #17e8b7;
		font-size: 14px;
	}

	.wrapper {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100vh;

		.inner-wrapper {
			margin-bottom: 20px;
		}
	}

	h1 {
		color: #caffef;
		font-weight: bold;
		font-size: 36px;
	}

	.logo {
		margin: 0px 0px 38px 0px;
		animation: floater 6s infinite;
	}

	.section {
		margin: 0px 0px 14px 0px;
	}

	.section-end {
		margin: 0px 0px 42px 0px;
	}
</style>
