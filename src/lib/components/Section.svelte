<script type="ts">
	export let padding: 'small' | 'medium' | 'large' = 'medium';
	export let noTopPadding: Boolean = false;
	export let noBottomPadding: Boolean = false;
</script>

<section class={padding} class:noTopPadding class:noBottomPadding>
	<slot />
</section>

<style>
	.small {
		padding-block: var(--section-padding-small, 2rem);
	}
	.medium {
		padding-block: var(--section-padding-medium, 4rem);
	}
	.large {
		padding-block: var(--section-padding-large, 6rem);
	}
	.noTopPadding {
		padding-block-start: 0;
	}
	.noBottomPadding {
		padding-block-end: 0;
	}
</style>
