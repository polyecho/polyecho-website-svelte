<script lang="ts">
	export let logo: string;
	export let url: string;
</script>

<a class="wrapper" href={url} target="_blank">
	<img alt="github logo" src={logo} />
</a>

<style lang="scss">
	.wrapper {
		margin: 0px 11px 0px 0px;
	}

	img {
		height: 42px;
		width: 42px;

		transform: scale(1);
		transition: 0.25s ease-in-out;
		transition-property: transform;

		&:hover {
			transform: scale(1.15);
		}
	}
</style>
