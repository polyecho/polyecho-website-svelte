<script lang="ts">
	export let logo: string;
	export let url: string;
</script>

<a class="wrapper" href={url} target="_blank">
	<img alt="github logo" src={logo} />
</a>

<style lang="scss">
	a {
		text-decoration: none;
	}

	.wrapper {
		margin-right: 13px;

		img {
			height: 42px;
			width: 42px;

			transform: scale(1);
			transition: 0.3s ease-in-out;
			transition-property: transform;

			&:hover {
				transform: scale(1.2);
			}
		}
	}
</style>
