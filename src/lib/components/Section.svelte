<script type="ts">
	export let padding: 'small' | 'medium' | 'large' = 'medium';
	export let noTopPadding = false;
	export let noBottomPadding = false;
</script>

<section class={padding} class:noTopPadding class:noBottomPadding>
	<slot />
</section>

<style>
	.small {
		padding-block: var(--section-padding-s, 2rem);
	}
	.medium {
		padding-block: var(--section-padding-m, 4rem);
	}
	.large {
		padding-block: var(--section-padding-m, 6rem);
	}
	.noTopPadding {
		padding-block-start: 0;
	}
	.noBottomPadding {
		padding-block-end: 0;
	}
</style>
